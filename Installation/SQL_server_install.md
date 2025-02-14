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
--------------------------------------------------

## Step 02: :Install SQL Server Command Line Tools (sqlcmd)

## 2.1: Install the Client Tools
        wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
        sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/prod.list)"
        sudo apt update
        sudo apt install -y mssql-tools unixodbc-dev
![image](https://github.com/user-attachments/assets/54767921-a48c-47e2-9923-309b336a306f)

## 2.2: Add sqlcmd to PATH
        echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bashrc
        source ~/.bashrc
## 2.3: Test SQL Server Connection
        sqlcmd -S localhost -U SA -P 'Password'

If is's working successfully , we can see below output 
![image](https://github.com/user-attachments/assets/00045311-041a-4053-90d9-e5272a7d1209)


        
