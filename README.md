# Zebra-Printer-Set-RFID-Config-file-in-E-Drive

# ZT411R のRFID設定ファイル登録方法　　

<p>
（事前） 印字ヘッド、プラテンローラに汚れ、損傷がないか目視確認する
1. 印字圧力 を調整する
2. 用紙センサーの位置を適切な位置に設定する
3. 用紙のキャリブレーションをする。キャリレーション後はフィードボタンを押下し、フィード毎に同じところに停止するか確認する。
4. RFIDキャリブレーションor コマンド（^XA^HR^XZ）実施。
5．下記設定値を確認
! U1 getvar "rfid.reader_1.antenna_port"
! U1 getvar "rfid.position.program"
! U1 getvar "rfid.reader_1.power.read"
! U1 getvar "rfid.reader_1.power.write"

6. 上記設定値を下記に代入し、下記4行をSETUP01.ZPLとして保存する。
※最終行にはCRLFを追加すること
! U1 setvar "rfid.reader_1.antenna_port" "E4"
! U1 setvar "rfid.position.program" "F5"
! U1 setvar "rfid.reader_1.power.read" "30"
! U1 setvar "rfid.reader_1.power.write" "30"

7. SETUP.ZPLをUSBメモリのルートにコピーする
8. ZT411液晶画面の操作で、USBメモリ\SETUP01.ZPLをプリンタのEドライブにコピーする。
　メニュー＞フォルダ＞USB> Copy Files to Printer > SETUP01.ZPL

これで、液晶画面からSETUP01.ZPLに記述した設定を反映させることができるようになります。
メニュー＞フォルダ＞USB> Eから印刷 > SETUP01.ZPL

</p>
