To switch between modes (i.e. serial output raw from camera, qr codes, others), everytime the ESP32 board is reset it waits for few milliseconds for a character that defines which mode:

    while (waitForStreamMode > millis()) {
        if (Serial.available())  // if we receive anything, just switch to another mode
        {
          switch (Serial.read()) {
            case 'q':  // QR code reader mode
              qr_reader_setup();
              for (;;)
                qr_reader_loop();

            case 'm':  // Motion detection
              motion_detection_setup();
              for (;;)
                motion_detection_loop();
    ...

Check [esp32cam_marauder.ino](https://github.com/eried/flipperzero-mayhem/blob/master/esp32cam_marauder/esp32cam_marauder.ino) file for the actual code. This makes switching mode easy in the Flipper fap, turning off and on the _otg_ power and sending the corresponding `char` for which mode we want to use in the app:

    furi_hal_power_disable_otg();
    furi_delay_ms(200);
    furi_hal_power_enable_otg();
    furi_delay_ms(500); 
    furi_hal_uart_tx(FuriHalUartIdUSART1, (uint8_t[1]){'q'}, 1);
    ...

Check the [companion apps](https://github.com/eried/flipperzero-mayhem/tree/master/flipper_companion_apps) for the actual code.