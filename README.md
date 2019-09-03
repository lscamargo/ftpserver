# ftpserver
A small tutorial on how to set up a ftp server on Debian with vsFTPd

1 Install vsftpd and ftp
```
sudo apt install vsftpd ftp
```

2 Backup config file
```
mv /etc/vsftpd.conf /etc/vsftpd.conf.bak
```

3 Copy files to /etc
```
cp vsftpd.conf vsftpd.userlist /etc
```

4 Start vsftpd
```
sudo systemctl start vsftpd
```

5 Create ftp folder
```
sudo mkdir /var/ftp
sudo chown ftp.ftp /var/ftp
sudo chmod 755 /var/ftp
```

6 Start ftp connection
```
ftp -p <IP>
```

* login: anonymous.
* No password is required.
* Simple commands are: cd, ls, get and put.
