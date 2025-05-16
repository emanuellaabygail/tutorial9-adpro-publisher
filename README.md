# Tutorial 9 Adpro 
**Emanuella Abygail - 2306152185**

## How much data your publisher program will send to the message broker in one run?
5 kali karena pada `main.rs` terdapat lima `publish_event` dan setiap `publish_event` mengirim satu `UserCreatedEventMessage` ke message broker.

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
Both publisher dan subscriber memanggil ke server AMQP yang sama. Keduanya berkomunikasi dengan message broker yang sama sehingga pesam yang dikirim publisher akan diterima oleh subscriber melalui server AMQP tersebut.

## Running RabbitMQ
![Running RabbitMQ](image.png)

## Sending and Processing Event
![rocessing Event](image-1.png)
Terminal pertama adalah menjalankan message broker yaitu RabbitMQ. Terminal kedua dan ketiga adalah menjalankan subscriber dan publisher dengan `cargo run`. Publisher yang berjalan akan mengirimkan data ke message broker lalu subscriber menerima data tersebut. Hal ini terlihat pada gambar.

## Monitoring Chart Based On Publisher
![Monitoring Chart](image-2.png)
Gambar di atas adalah ketika saya memanggil `cargo run` pada publisher beberapa kali. Dari gambar tersebut, dapat disimpulkan bahwa ketika publisher mengirimkan data, message rates akan meningkat dan message broker menerima banyak data dari publisher.