# Tutorial 9 Adpro 
**Emanuella Abygail - 2306152185**

## How much data your publisher program will send to the message broker in one run?
5 kali karena pada `main.rs` terdapat lima `publish_event` dan setiap `publish_event` mengirim satu `UserCreatedEventMessage` ke message broker.

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
Both publisher dan subscriber memanggil ke server AMQP yang sama. Keduanya berkomunikasi dengan message broker yang sama sehingga pesam yang dikirim publisher akan diterima oleh subscriber melalui server AMQP tersebut.