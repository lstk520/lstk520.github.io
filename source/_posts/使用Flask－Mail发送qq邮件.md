---
title: 使用Flask－Mail发送qq邮件
date: 2017-02-22 11:05:36
tags: flask
---

http://www.jianshu.com/p/32e2f82a63c3

废话不多说，直接上代码：

from flask import Flaskfrom

flask_mail import Mail, Message

app = Flask(__name__)

app.config.update(   

      #EMAIL SETTINGS   

     MAIL_SERVER='smtp.qq.com',   

     MAIL_PORT=465,  

     MAIL_USE_SSL=True,  

    MAIL_USERNAME = 'qq号(如：123456)',  

     MAIL_PASSWORD = 'qq邮箱授权码'    )






mail = Mail(app)

@app.route("/")

def index():   

     msg = Message(subject="helloworld", sender='发送邮箱地址(如：123456@qq.com)', recipients=['接受邮箱地址(如：654321@qq.com)'])    

     msg.html = "testinghtml"   

     mail.send(msg)   



if__name__ =='__main__':

    app.run(debug=True)
