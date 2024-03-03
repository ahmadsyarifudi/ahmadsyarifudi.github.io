---
layout: page
title: The Work of a Process
description: Designing a System Program for AVR Microcontrollers That Can Used to Regulate The  Work of a Process Unit
img: assets/img/12.jpg
importance: 1
category: work
related_publications: true
---

Dua jenis larutan kimia akan dimasukkan pada tanki penyimpan (storage tank), kemudian  dipanaskan dan diaduk, dan akhirnya dialirkan keluar untuk ke proses berikutnya. Seperti terlihat  pada gambar, pada unit tsb terdapat beberapa sensor (input) dan actuator (output) yang akan  digunakan oleh microcontroller untuk mengendalikan proses yang akan dilakukan. Dalam kondisi  normal (sistem tidak bekerja), semua valve dalam kondisi tertutup dan begitu juga Heater dan  Pengaduk dalam kondisi mati.

this project pdf [here](https://drive.google.com/file/d/10qAKELwr0HBtpwgwk3e-BjsHP0C6eV2l/view?usp=drive_link)

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project/project1/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Desain rangkaian pada protheus
</div>
Tombol START harus ditekan untuk memulai proses. Mula-mula larutan 1 dan larutan 2 harus  diisikan ke dalam tanki dengan cara membuka valve INFLOW1 dan INFLOW2 sampai sensor  TANKFUL= ‘1’ (aktif) yang berarti bahwa level larutan sudah mencapai level yang diinginkan  dan valve INFLOW1 dan INFLOW2 kemudian ditutup. Setelah itu Heater dinyalakan melalui  HTRON dan Pengaduk juga dihidupkan melalui STIRON , keduanya terus dihidupkan sampai  temperatur larutan yang diinginkan tercapai, yaitu pada saat sensor TEMPOK = ‘0’ (aktif). 

Campuran larutan yang telah dipanaskan tersebut kemudian dialirkan ke proses selanjutnya  melalui valve OUTFLOW, dan valve OUTFLOW akan ditutup setelah sensor TANKMT = ‘0’  (aktif), dan seterusnya keseluruhan proses akan berulang lagi, jika tombol HOLD tidak ditekan  sebelumnya. Jika tombol HOLD ditekan, sistem akan berhenti untuk sementara dan sistem akan  berjalan lagi melakukan siklus proses yang sama, jika tombol START ditekan kembali. Selain itu,  sistem ini juga dilengkapi dengan ‘emergency SHUTDOWN switch’. Jika tombol tsb ditekan,  maka processor akan diinterupsi melalui jalur INT0 , yang akan menghentikan proses apapun yang  sedang berlangsung dan lampu ALARM serta BUZZER akan aktif (ON).
