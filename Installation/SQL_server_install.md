## Installation 
# SQL_DW_Project | SQL server & SSMS install guide and steps 
SQL data Warehouse Project 

## Install SQL server in Ubuntu 20.04 


1:Add the Microsoft SQL Server Repository
        wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
        sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2022.list)"
    
## 2: Install SQL Server
        sudo apt update
        sudo apt install -y mssql-server
    
## 3: Run SQL Server Configuration
        sudo /opt/mssql/bin/mssql-conf setup
![image](https://github.com/user-attachments/assets/098e5fe8-35e3-4f74-b136-a500c714cea5)


        
## 4: Start & Enable SQL Server
        sudo systemctl start mssql-server
        sudo systemctl enable mssql-server
    
## 5: Verify SQL Server is Running
        systemctl status mssql-server
