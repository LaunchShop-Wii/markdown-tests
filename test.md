# Rii Shop Channel. DEVELOPMENT PRIVATE EDITION
This is a revival of the now dead Wii Shop Channel.
Our goal is to make
The first time you load the RSC Server in PC mode (Non-HTTPS), You will see this page.
![](https://github.com/theDtubeTeam/WSC_SRVROOT/blob/main/image.png?raw=true)<br>
Looks pretty good, right!
# features
- P

# how to run
To run the server, You must install <a href="https://www.python.org/downloads/">Python</a> to run the app.<br>
Once <a href="https://www.python.org/downloads/">Python</a> is installed, open a terminal window (cmd.exe for windows), and do ``` pip install --upgrade pip ``` to update pip to it\'s latest version.<br>
Then run these commands to install Flask and Flask_babel.<br>
```
pip install flask
pip install flask_babel
```
# PC Mode \(Non-HTTPS\)
As we currently do not provide the WAD, You must change this line in ``` app.py ``` from
```python
app.run(host=socket.gethostbyname(socket.gethostname()), port=443, debug=True, ssl_context=context)
```
to
```python
app.run(host=socket.gethostbyname(socket.gethostname()), port=80, debug=True)
```

```
py app.py
```
IF you are running the payment server, don't run the server in PC mode, and also run payment.py, You may need to change the IP's at the end of payment.py and app.py.
```python
py payment.py
```
Open your web browser and navigate to the url specified from the output of app.py. Ex,
```
* Running on http://192.168.<>.<>:80
```
# Payment Server payments. Here is the URL:
```txt
http://<the server ip>:80/payment_interface/info/<First part of your wii serial number>/<The randomly generated token>
```
<br>

# YOU WILL NOT BE CHARGED IN DEVELOPMENT MODE
```http
YOU WILL NOT BE CHARGED IN DEVELOPMENT MODE
```
Paypal MUST be kept in sandbox mode for development apps. Meaning if you enter your number and click pay, you will not be charged. Paypal will just emulate a successful payment without charging you.
