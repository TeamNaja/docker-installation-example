# docker-installation-example
ขั้นตอนการติดตั้ง Docker Desktop บน Windows
เดี่ยวอนาคตมีของ Docker Desktop บน Linux 

1. Docker Desktop คือหยัง 
Docker Desktop คือ Docker ไม่ใช่ Doggy หยอก 

Docker Desktop คือ  โปรแกรมเอาไว้จัดการ container ที่อยู่ในเครื่องเรา 
โดย docker จะจำลอง environment ขึ้นมาบน WSL* (Windows Subsystems for Linux)
อยากรู้หาอ่านเอง หรือถามเอาละกัน ค้านพิมพ์

2. เปิด Powershell ขึ้นมา หน้าตามันสิเป็นจั่งซี่  Run as admin นะ
![image](https://user-images.githubusercontent.com/71694878/131340136-1a1f8751-a13a-4a08-973b-db28425bc4b4.png)
![image](https://user-images.githubusercontent.com/71694878/131340153-af033667-8e74-4ecb-81aa-597a291f317b.png)


3. ใส่คำสั่งนี้เข้าไปเพื่อ เปิด WSL ก่อน
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
![image](https://user-images.githubusercontent.com/71694878/131340297-b51d3e66-f87c-4965-9eb8-226d016469bd.png)


4. ต่อด้วยคำสั่งนี้ 
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
![image](https://user-images.githubusercontent.com/71694878/131340451-d9f537af-47b5-4496-be02-85c5d27c7092.png)


4.5 Restart อีกทีได้ไหม  อีกแค่สักครั้งงง   ถ้าจำเป็นนะ

5. Download ไฟล์นี้ แล้วติดตั้ง
https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
![image](https://user-images.githubusercontent.com/71694878/131340554-6a1991f0-e4b5-432e-a927-bd143b3b5234.png)


6. กลับมาที่ powershell อีกครั้ง run คำสั่งนี้ 
wsl --set-default-version 2
![image](https://user-images.githubusercontent.com/71694878/131340641-a6d455c0-8404-4b0c-aa9a-a24f417aa4c8.png)


7. เปิด Microsoft Store 
หา ubuntu ที่เป็น lts (long term support คือ version ที่ support 8 ปี) 
![image](https://user-images.githubusercontent.com/71694878/131340768-fdf693d1-518a-4edb-8528-3395f93b5269.png)
![image](https://user-images.githubusercontent.com/71694878/131340793-2f35fdf5-7374-44bf-b49b-5f97c7a299ee.png)
![image](https://user-images.githubusercontent.com/71694878/131340833-87112d9c-8b19-43cf-8944-df702c052293.png)


8. เปิด ubuntu ขึ้นมา มันจะให้ใส่ username password กะใส่เอาโล้ด จำไว้นำ
![image](https://user-images.githubusercontent.com/71694878/131341038-31eb883b-4318-4d60-a2e1-ca0fd4228d1e.png)
![image](https://user-images.githubusercontent.com/71694878/131341059-3720d73d-e25a-429c-9b7f-9ddd8cb46afd.png)


9. แล้วแล้วก็ Download Docker Desktop มา
https://www.docker.com/products/docker-desktop
![image](https://user-images.githubusercontent.com/71694878/131341261-f3fe86e6-044b-4bf7-a414-cf8697dbc6b4.png)
(ย้านบ่เห็น)


10. ติดตั้งโล้ด ข่อยลงแล้ว
![image](https://user-images.githubusercontent.com/71694878/131341425-a0f4a369-9e21-43fe-ae10-775186e01ee3.png)


11. เปิดขึ้นมาบานนิ มันจะเป็นจั่งซี่
![image](https://user-images.githubusercontent.com/71694878/131341490-20a85583-cc33-4eef-960b-51eab07a260b.png)


12. ไผติดหยัง ไปเปิด Issue ไว้ เดี๋ยวจะบอกวิธี

ref :
https://docs.microsoft.com/en-us/windows/wsl/install-win10

