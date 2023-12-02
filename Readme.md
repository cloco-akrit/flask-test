```
#!/bin/bash
yum install git -y
yum install gcc -y
yum install python3-devel -y
cd /opt && git clone https://github.com/cloco-akrit/flask-test.git
chown -R ec2-user:ec2-user /opt/flask-test
cd /opt/flask-test && python3 -m ensurepip
cd /opt/flask-test && python3 -m pip install -r requirements.txt
chmod +x /opt/flask-test/start.sh
/opt/flask-test/start.sh
```
