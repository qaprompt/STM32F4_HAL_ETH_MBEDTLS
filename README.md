# STM32F4_HAL_ETH_MBEDTLS
STM32F4 HAL mbedTLS library testing (SSL/TLS client)

1. Reference 
https://engschool.tistory.com/entry/SSLTLS-embedded-for-IoT-8
https://cxemotexnika.org/2018/10/primer-zashhishhennogo-https-soedineniya-s-ispolzovaniem-mbed-tls/
https://github.com/PetroShevchenko/cxemotexnika/tree/master/Examples/NUCLEO_F429ZI/nucleo_f429zi_https_client

2. Tutorial [Written in Korean]
https://blog.naver.com/eziya76/221959527368
https://blog.naver.com/eziya76/221963225897

3. Issue
I found a memory leak issue when "mbedtls_ssl_handshake" is called and haven't solved it yet.
To walk around this issue, I used "mbedtls_memory_buffer_alloc_init" and recreate SSL task whenever memory error happens.
