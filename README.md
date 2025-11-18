# OPEN-SOURCE-EX-2
## NAME : KARTHICKKUMAR R
## REG NO : 212223040087
## DEPT : CSE
# STEPS INVOLVED:

### STEP 1 : sudo ss -tuln | grep :82
### STEP 2 : LISTEN  0  128  *:82  *:*  
### STEP 3 : getenforce
### STEP 4 : 
```
ls -Zd /var/www/html
drwxr-xr-x. root root system_u:object_r:httpd_sys_content_t:s0 /var/www/html
sudo restorecon -Rv /var/www/html

semanage port -l | grep http_port_t
sudo semanage port -a -t http_port_t -p tcp 82
sudo semanage port -m -t http_port_t -p tcp 82

sudo systemctl status httpd
sudo firewall-cmd --list-all
sudo firewall-cmd --add-port=82/tcp --permanent
sudo firewall-cmd --reload
```
### STEP 5 : http://<your-server-ip>:82
# OUTPUT :


<img width="1145" height="848" alt="image" src="https://github.com/user-attachments/assets/32d2888b-1d7d-48da-8514-8c232d6e7225" />

<img width="1268" height="890" alt="image" src="https://github.com/user-attachments/assets/54cacdaf-0718-4b72-9c03-746fadbd01cf" />

<img width="1153" height="864" alt="image" src="https://github.com/user-attachments/assets/3647bdef-5d71-4c43-bb30-781b7542dd9d" />

<img width="761" height="550" alt="image" src="https://github.com/user-attachments/assets/9c7a90ef-940d-4b8b-8429-a5db71bdcea7" />

<img width="1026" height="829" alt="image" src="https://github.com/user-attachments/assets/8259321e-62cc-4eab-8118-ff62b52451c6" />

<img width="1062" height="353" alt="image" src="https://github.com/user-attachments/assets/8913cef4-828f-4005-9b9b-9b96a3b165e1" />

<img width="734" height="508" alt="image" src="https://github.com/user-attachments/assets/89b9e1c5-97c7-4d79-a1b6-dd05c1cf4a7a" />

<img width="722" height="526" alt="image" src="https://github.com/user-attachments/assets/56462e75-5f8b-499d-998a-d2c1e13cc65a" />

# RESULT : 
Thus the commands worked properly in RedHat Terminal(Lab)
