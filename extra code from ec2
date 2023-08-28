import os
import mysql.connector
from flask import Flask
app = Flask(__name__)

@app.route("/")
def main():
    return "Welcome!"

@app.route('/how are you')
def hello():
    return 'I am good, how about you?'

@app.route('/getUsers')
def users():
    conn = mysql.connector.connect(user='meg', password='meg12345', host='127.0.0.1', database='mysql',auth_plugin='mysql_native_password')

    cursor = conn.cursor()
    sql = '''SELECT * from users'''
    cursor.execute(sql)


    result = cursor.fetchall()
    return result

    conn.close()

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=8081)

