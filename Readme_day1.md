<!-- TOC -->

- [การติดตั้ง Evironment และชุดเครื่องมือในการพัฒนา](#การติดตั้ง-evironment-และชุดเครื่องมือในการพัฒนา)
    - [ติดตั้ง Node.js](#ติดตั้ง-nodejs)
        - [ติดตั้งบน Windows](#ติดตั้งบน-windows)
            - [วิธีการติดตั้ง](#วิธีการติดตั้ง)
        - [ติดตั้งบน OSX](#ติดตั้งบน-osx)
        - [ติดตั้งบน Linux](#ติดตั้งบน-linux)
    - [ติดตั้งเครื่องมือที่ใช้ในการพัฒนา](#ติดตั้งเครื่องมือที่ใช้ในการพัฒนา)
        - [Visual Studio Code](#visual-studio-code)
        - [Install Extension](#install-extension)
            - [Install Extension](#install-extension-1)
        - [Additional Platforms](#additional-platforms)
    - [Node.js คืออะไร?](#nodejs-คืออะไร)
    - [Node.js Architecture](#nodejs-architecture)
        - [Single Threaded Event Loop](#single-threaded-event-loop)
        - [Node Cluster Module](#node-cluster-module)
        - [Prodution Process Manger Module](#prodution-process-manger-module)
    - [Hello World!](#hello-world)
- [JavaScript Fundamentals](#javascript-fundamentals)
    - [ตัวแปรใน JavaScript](#ตัวแปรใน-javascript)
    - [การทำงานแบบ Synchronous และ Asynchronous](#การทำงานแบบ-synchronous-และ-asynchronous)
    - [Callback to Promise](#callback-to-promise)
        - [References](#references)
- [Node.js Fundamentals](#nodejs-fundamentals)
    - [Using Require](#using-require)
    - [Requiring Your Own Files](#requiring-your-own-files)
    - [Using 3rd Party Modules](#using-3rd-party-modules)
    - [Restarting App with Nodemon](#restarting-app-with-nodemon)
    - [Workshop สร้างเว็บแอปพลิเคชันเพื่อบริการ Static File](#workshop-สร้างเว็บแอปพลิเคชันเพื่อบริการ-static-file)
    - [Workshop เพิ่มความปลอดภัยให้เว็บแอปพลิเคชันที่ให้บริการ Static File ด้วย HashIds](#workshop-เพิ่มความปลอดภัยให้เว็บแอปพลิเคชันที่ให้บริการ-static-file-ด้วย-hashids)
    - [Workshop สร้าง RESTFul API ด้วย Express.js](#workshop-สร้าง-restful-api-ด้วย-expressjs)
    - [วิธีการทำ NodeJS แยก config ระหว่าง dev กับ production](#วิธีการทำ-nodejs-แยก-config-ระหว่าง-dev-กับ-production)

<!-- /TOC -->
# การติดตั้ง Evironment และชุดเครื่องมือในการพัฒนา
## ติดตั้ง Node.js
![](images/2018-06-08-11-11-36.png#center)
### ติดตั้งบน Windows

* LTS Version (8.11.2)
  * 32-bit https://nodejs.org/dist/v8.11.2/node-v8.11.2-x86.msi
  * 64-bit https://nodejs.org/dist/v8.11.2/node-v8.11.2-x64.msi
* Current Version (10.4.0)
  * 32-bit https://nodejs.org/dist/v10.4.0/node-v10.4.0-x86.msi
  * 64-bit https://nodejs.org/dist/v10.4.0/node-v10.4.0-x64.msi

#### วิธีการติดตั้ง
**Step 1**
หลังจากทำการดาวน์โหลดมาเรียบร้อยแล้วให้ทำการติดตั้งโดยการ Double click ที่ไฟล์ .msi

![](images/2018-06-08-11-22-58.png#center)

**Step 2**
ทำการเลือก default location หรือหากต้องการเปลี่ยนก็สามารถทำได้จากหน้าจอนี้
![](images/2018-06-08-11-23-12.png#center)

**Step 3**
รอจนกว่าโปรแกรมจะทำการ Install เสร็จ

![](images/2018-06-08-11-23-19.png#center)

**Step 4**
เมื่อขั้นตอนการติดตั้ง Node.js สำเร็จแล้ว ให้คลิกเสร็จเสร็จสิ้น และเพื่อให้การทำงานที่สมบูรณ์ให้ทำการ Restart เครื่องคอมพิวเตอร์

![](images/2018-06-08-11-23-29.png#center)

References
* [Technicalkeeda.com](http://www.technicalkeeda.com/nodejs-tutorials/how-to-install-node-js-on-windows)


### ติดตั้งบน OSX

* LTS Version (8.11.2)
  * 64-bit https://nodejs.org/dist/v8.11.2/node-v8.11.2.pkg
* Current Version (10.4.0)
  * 64-bit https://nodejs.org/dist/v10.4.0/node-v10.4.0.pkg

สามารถติดตั้งผ่าน package ของ .dmg ได้ตามขั้นตอน

![](images/2018-06-08-11-27-40.png#center)

หลังจากติดตั้งแล้ว สามารถตรวจสอบว่าสามารถใช้งานผ่าน Terminal ได้หรือไม่ด้วยคำสั่งอย่างง่ายดังนี้

```
node

> console.log('hello node');

hello node

undefined

>
```

หรือตรวจสอบเลขเวอร์ชันได้ด้วยคำสั่งดังนี้

```
node -v
```

References
* [coolestguidesontheplanet.com](https://coolestguidesontheplanet.com/installing-node-js-on-macos/)

### ติดตั้งบน Linux
* LTS Version (8.11.2)
  * 32-bit https://nodejs.org/dist/v8.11.2/node-v8.11.2-linux-x86.tar.xz
  * 64-bit https://nodejs.org/dist/v8.11.2/node-v8.11.2-linux-x64.tar.xz
* Current Version (10.4.0)
  * 64-bit https://nodejs.org/dist/v10.4.0/node-v10.4.0-linux-x64.tar.xz

1) เปิด Ubuntu terminal
![](images/2018-06-08-11-33-43.png#center)

2) ติดตั้ง Node.js ด้วยคำสั่ง `sudo apt-get install python-software-properties`

3) กด Enter (If you have set a password for your system then it will ask for the password)

4) พิมพ์รหัสผ่านแล้วกด Enter
![](images/2018-06-08-11-33-48.png#center)
5) พิมพ์คำสั่ง `sudo apt-add-repository ppa:chris-lea/node.js`

6) กด Enter
![](images/2018-06-08-11-33-53.png#center)
7) กด Enter อีกครั้ง
8) พิมพ์คำสั่ง `sudo apt-get update` ( Wait for sometime)
![](images/2018-06-08-11-35-04.png#center)
9) พิมพ์คำสั่ง `sudo apt-get install nodejs npm`
![](images/2018-06-08-11-35-23.png#center)
10) พิมพ์คำสั่ง `sudo apt-get install nodejs`
![](images/2018-06-08-11-36-53.png#center)
เมื่อติดตั้งสำเร็จ สามารถตรวจสอบหมายเลขเวอร์ชันได้ด้วยคำสั่ง `node --version`
![](images/2018-06-08-11-37-22.png#center)


References
* [javatpoint.com](https://www.javatpoint.com/install-nodejs-on-linux-ubuntu-centos)

## ติดตั้งเครื่องมือที่ใช้ในการพัฒนา
### Visual Studio Code

 **Visual Studio Code** หรือ **VSCode** เป็นโปรแกรม Code Editor ที่ใช้ในการแก้ไขและปรับแต่งโค้ด จากค่ายไมโครซอฟท์ มีการพัฒนาออกมาในรูปแบบของ OpenSource จึงสามารถนำมาใช้งานได้แบบฟรี ๆ ไม่มีค่าใช้จ่ายและสามารถพัฒนาซอฟต์แวร์ในเชิงพานิชย์ได้ ที่ต้องการความเป็นมืออาชีพ ซึ่ง Visual Studio Code นั้น เหมาะสำหรับนักพัฒนาโปรแกรมที่ต้องการใช้งานข้ามแพลตฟอร์ม รองรับการใช้งานทั้งบน Windows, macOS และ Linux สนับสนุนทั้งภาษา JavaScript, TypeScript และ Node.js สามารถเชื่อมต่อกับ Git ได้ นำมาใช้งานได้ง่ายไม่ซับซ้อน มีเครื่องมือส่วนขยายต่าง ๆ ให้เลือกใช้อย่างมากมาก ไม่ว่าจะเป็น 1.การเปิดใช้งานภาษาอื่น ๆ ทั้ง ภาษา C++, C#, Java, Python, PHP หรือ Go 2.Themes 3.Debugger 4.Commands เป็นต้น
https://code.visualstudio.com/download

![](images/2018-06-08-12-00-23.png#center)

![](images/2018-06-08-11-55-41.png#center)


### Install Extension
#### Install Extension
* Node.js Extension Pack.
>https://marketplace.visualstudio.com/items?itemName=waderyan.nodejs-extension-pack

![](images/nodejs_extension_pack.png#center)


* Beautify
>https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify

![](images/nodejs_extension_buautify.png#center)


* JavaScript extensions for VS Code
>https://code.visualstudio.com/docs/nodejs/extensions

![](images/nodejs_extension_other.png#center)

### Additional Platforms
* SunOS Binaries
  * 32-bit https://nodejs.org/dist/v10.4.0/node-v10.4.0-sunos-x86.tar.xz
  * 64-bit https://nodejs.org/dist/v10.4.0/node-v10.4.0-sunos-x64.tar.xz
* Docker Image https://hub.docker.com/_/node/
* Linux on Power Systems https://nodejs.org/dist/v10.4.0/node-v10.4.0-linux-ppc64le.tar.xz
* Linux on System z https://nodejs.org/dist/v10.4.0/node-v10.4.0-linux-s390x.tar.xz
* AIX on Power Systems https://nodejs.org/dist/v10.4.0/node-v10.4.0-aix-ppc64.tar.gz
## Node.js คืออะไร?
Node.js เป็นภาษา Javascript ตัวหนึ่งที่สามารถทำงานได้ทั้งฝั่ง Server และ Client โดยรวม Environment ต่างๆ ที่ทำขึ้นเพื่อให้เราเขียน JavaScript เอาไว้ที่ฝั่ง Server ได้ด้วย (Webserver, Runtime และอื่นๆ) เรียกได้ว่ามันคือ Platform และจุดเด่นของ Node.js คือความเร็วในการประมวลผล ซึ่งระบบที่พัฒนาด้วย Node.js นั้นจะมีความเร็วมากกว่าภาษาอื่นๆ อย่างเห็นได้ชัด จึงทำให้ Node.js นั้นเป็นที่นิยมอย่างแพร่หลายในปัจจุบัน
## Node.js Architecture
### Single Threaded Event Loop

![](images/2018-06-13-05-30-51.png#center)

### Node Cluster Module
ด้วย Architechture แบบ Single Instance ของ Node.js จะทำงานแบบ single thread แต่หากระบบที่มีการทำงานแบบmulti-core systems ผู้ใช้ก็จะสามารถใช้ความสามารถของ cluster ของ Node.js ในการประมวลผลเพื่อช่วยเพิ่มประสิทธิภาพการทำงานได้

การใช้งาน cluster module จะเป็นการขยาย child processes เพื่อให้เกิด process ตามจำนวน Core ของ CPU ซึ่งสามารถทำได้ง่าย ๆ โดยแสดงตัวอย่างจากโค้ดด้านล่าง

```js
const cluster = require('cluster');
const http = require('http');
const numCPUs = require('os').cpus().length;

if (cluster.isMaster) {
  console.log(`Master ${process.pid} is running`);

  // Fork workers.
  for (let i = 0; i < numCPUs; i++) {
    cluster.fork();
  }

  cluster.on('exit', (worker, code, signal) => {
    console.log(`worker ${worker.process.pid} died`);
  });
} else {
  // Workers can share any TCP connection
  // In this case it is an HTTP server
  http.createServer((req, res) => {
    res.writeHead(200);
    res.end('hello world\n');
  }).listen(8000);

  console.log(`Worker ${process.pid} started`);
}
```
Running Node.js will now share port 8000 between the workers:
จากนั้นให้ทำการทดสอบรัน Application ซึ่ง Node.js จะเพิ่มการทำการเพิ่ม Child Process Workers ให้อัตโนมัติตามจำนวน CPU Core ดังนี้

```
$ node server.js
Master 3596 is running
Worker 4324 started
Worker 4520 started
Worker 6056 started
Worker 5644 started
```

### Prodution Process Manger Module
นอกจากการทำงานของ Cluster Module จะช่วยให้เราสามารถเพิ่มประสิทธิภาพการทำงานของ Node.js ได้แล้ว เรายังสามารถใช้  3rd Module เช่น PM2  ในการช่วยจัดการ Process ได้ง่าย ๆ โดยไม่ต้องทำการปรับเปลี่ยนชุด Source-Code เลย ซึ่งมีขั้นตอนการใช้งานดังนี้่

ติดตั้ง pm2 module แบบ Global ด้วยคำสั่ง
```
npm install pm2 -g
```

จากนั้นเมื่อต้องการรัน Application เราก็อาศัย pm2 ในการรันแอปพลิเคชันแทน Node.js ดังนี้
```
pm2 start app.js -i 4
```

pm2 จะทำการขยาย Application ของเราให้ทำงานแบบ Cluster ได้ทันทีดังภาพด้านล่าง

![](images/2018-06-13-05-58-35.png#center)


## Hello World!
1. สร้าง Folder ชื่อ *lab1* ที่ `c:\nodejs\`
2. สร้างไฟล์ชื่อ *index.js* ที่ `c:\nodejs\lab1`
3. พิมพ์ Code JavaScript ดังนี้

![](images/2018-06-13-21-26-23.png#center)

4. เปิด Terminal และทดลองรันโปรแกรมด้วยคำสั่ง `node index.js`
5. หลังจากนั้นทดลองดูผลการการทำงานของ node.js โดยให้ทำการเปิดเว็บเบราว์เซอร์ โดยเข้าไปที่ `http://localhost:3000` หากไม่มีข้อผิดพลาด เราจะสามารถเห็นข้อความ `Hello World` ที่หน้าจอ
# JavaScript Fundamentals
10 อันดับ ภาษาที่ใช้เยอะที่สุด นับสถิติจากการใช้งานใน Github

Source: https://octoverse.github.com

![](images/2018-06-11-17-08-32.png#center)


TIOBE Index for June 2018
June Headline: TypeScript finally enters the TIOBE Index Top 100

Source: https://www.tiobe.com/tiobe-indexฝ

![](images/2018-06-11-17-11-22.png#center)

## ตัวแปรใน JavaScript
ใน JavaScript จะมีการประกาศตัวแปรอยู่ 4 แบบด้วยกัน คือใช้ var, let, const และไม่ระบุ

1. var คือ การประกาศตัวแปรสำหรับใช้ใน code ในส่วนที่ถูกรันในส่วนนั้นๆ อาจจะหมายถึงทั้ง function หรือทั้งไฟล์เลยก็เป็นได้
2. let คือ การประกาศตัวแปรสำหรับใช้เฉพาะใน scope นั้นหรือเฉพาะใน block นั้นๆ
3. const คือ การประกาศตัวแปรแบบค่าคงที่ หรือพูดง่ายๆคือตัวแปรแบบ Read Only
4. ไม่ระบุ คือ การประกาศแบบ global ** การประกาศตัวแปรแบบ global คือการประกาศเอาไว้ใน scope นอกสุดครับ **

```js
function varTest() {
  var x = 1;
  if (true) {
    var x = 2;  // มองเป็นตัวเดียวกันกับด้านนอก
    console.log(x);  // 2
  }
  console.log(x);  // 2
}

function letTest() {
  let x = 1;
  if (true) {
    let x = 2;  // มองเป็นคนละตัวกับด้านนอก
    console.log(x);  // 2
  }
  console.log(x);  // 1
}
varTest()
letTest()
console.log(x) // error
```

## การทำงานแบบ Synchronous และ Asynchronous
ทำความเข้าใจและทดลองเขียนโปรแกรมการทำงานของ JavaScript โดยจะลองใช้เครื่องมือที่ช่วยเขียน JavaScript ผ่าน Web browser ที่ https://jsfiddle.net/

![](images/2018-06-13-06-12-10.png#center)

พิมพ์ Code ที่ช่อง HTML ดังนี้
![](images/2018-06-13-06-16-27.png#center)
```
<div id="result"></div>
```

พิมพ์ Code ที่ช่อง JavaScript ดังนี้
![](images/2018-06-13-06-17-10.png#center)

จากนั้นให้ทดลอง Run เพื่อดูผลการทำงาน ซึ่งจะได้ดังนี้
![](images/2018-06-13-06-18-06.png#center)

ให้ทำการแก้ไข Code ที่ช่อง  JavaScript ดังนี้
![](images/2018-06-13-06-23-05.png#center)

จากนั้นให้ทดลอง Run เพื่อดูผลการทำงาน ซึ่งจะได้ดังนี้
![](images/2018-06-13-06-23-42.png#center)

## Callback to Promise
ทดลองเขียนโค้ดผ่าน https://jsfiddle.net/

เขียนโค้ดที่ช่อง JavaScript และทำการเลือก Library เป็น `JQuery 3.3.1`

![](images/2018-06-13-06-57-08.png#center)

ทำการรันโปรแกรมเพื่อดูผลการทำงาน

![](images/2018-06-13-06-44-37.png#center)

ซึ่งจะเห็นว่าผลการทำงานที่ได้ ไม่สามารถทำงานตามที่เราต้องการได้

ให้ทำการเพิ่มเติมโค้ดดังนี้
![](images/2018-06-13-06-56-21.png#center)

ทำการรันโปรแกรมเพื่อดูผลการทำงาน
![](images/2018-06-13-06-47-34.png#center)

จะเห็นว่า funtion plus ทำงานก่อนที่จะได้ค่า a,b 

ทำการเพิ่มโค้ดดังนี้
![](images/2018-06-13-06-53-41.png#center)

ทำการรันโปรแกรมเพื่อดูผลการทำงาน
![](images/2018-06-13-06-54-14.png#center)

ซึ่งผลการทำงานจะถูกต้อง แต่เกิดปัญหาการไล่หรือการทำความเข้าใจที่ซับซ้อนมาก จึงเกิด Concept ของ Promise ให้ทำการเขียนโค้ดในช่อง JavaScript ดังนี้ครับ

![](images/2018-06-13-07-04-01.png#center)

ทำการรันโปรแกรมเพื่อดูผลการทำงาน
![](images/2018-06-13-06-54-14.png#center)


### References
* [JavaScript. The Core: 2nd Edition](http://dmitrysoshnikov.com/ecmascript/javascript-the-core-2nd-edition/#object)
# Node.js Fundamentals
## Using Require

Build-In modules

```
mkdir notes-node
```
```
cd notes-node
```
สร้างไฟล์ app.js ใน VSCode

```js
console.log('Staring app.');

```
Open browser and open https://nodejs.org/api/ เลื่อนหาเพื่อเลือกใช้ modules ลองเข้าไปดู File System ลองใช้ fs.appendFile

```js
console.log('Staring app.');

const fs = require('fs');

// Option one
fs.appendFile('greetings.txt','Hello World',function(err){
    if(err){
      console.log('Unable ot write fo file');
    }
});

// Option two
//fs.appendFileSync('greetings.txt','Hello world!');

```

ทดลองรันเพื่อดูผลลัพธ์ ด้วยคำสั่ง `node app.js` หาไม่มีข้อผิดพลาดจะพบไฟล์ greetings.txt ที่ Directory เดียวกันกับไฟล์ `app.js` และมีเนื้อหาเป็น `Hello World!`


ทดลองใช้ Build-In modules ชื่อ `OS` โดยเปิด Web Browser ไปที่ https://nodejs.org/api/os.html และดูในหัวข้อ `os.userInfo` และเพิ่มโค้ดดังนี้

```js
console.log('Starting app.');

const fs = require('fs');
const os = require('os');

var user = os.userInfo();

console.log(user);
```
ทดลองรันดูผลลัพธ์ด้วยคำสั่ง `node app.js` หากไม่มีข้อผิดพลาดจะข้อมูลตามโครงสร้างตามนี้

![](images/2018-06-12-15-33-43.png#center)


จากนั้นทดลองนำข้อมูล
```js
console.log('Starting app.');

const fs = require('fs');
const os = require('os');

var user = os.userInfo();

fs.appendFileSync('greetings.txt','Hello ' + user.username + ' !');
```

ทดลองรันเพื่อดูผลลัพธ์

## Requiring Your Own Files
ให้เพิ่มไฟล์ `notes.js` และเพิ่มโค้ดดังนี้
```js
console.log('Starting notes.js');
```
กลับไปที่ไฟล์ app.js และ แก้ไขโค้ดดังนี้

```js
console.log('Starting app.js');

const fs = require('fs');
const os = require('os');
const notes = require('./notes.js');

var user = os.userInfo();

//fs.appendFileSync('greetings.txt','Hello ' + user.username + ' !');
```

 จากนั้นทดลองรันโปรแกรมด้วยคำสั่ง `node app.js` ซึ่งหากไม่มีข้อผิดพลาดจะเจอผลลัพธ์ดังนี้

 ![](images/2018-06-12-15-39-06.png#center)

 กลับที่ไฟล์ notes.js และเพิ่มโค้ดดังนี้

 ```js
 console.log('Starting notes.js');

 console.log(module);
 ```
 จากนั้นทดลองรันโปรแกรม

 ![](images/2018-06-12-15-42-43.png#center)

 ```js
console.log('Starting app.js');

const fs = require('fs');
const os = require('os');
const notes = require('./notes.js');

var user = os.userInfo();

//fs.appendFileSync('greetings.txt','Hello ' + user.username + ' !');
```

 กลับที่ไฟล์ notes.js และเพิ่มโค้ดดังนี้

 ```js
 console.log('Starting notes.js');

 module.exports.age = 25
 ```

 กลับที่ไฟล์ app.js และเพิ่มโค้ดดังนี้

 ```js
console.log('Starting app.js');

const fs = require('fs');
const os = require('os');
const notes = require('./notes.js');

var user = os.userInfo();

fs.appendFileSync('greetings.txt',`Hello ${user.username}! You are ${notes.age}`);
 ```
ทดลองรันโปรแกรม หากไม่เกิดข้อผิดพลาดจะได้ผลลัพธ์ ที่อยู่ในไฟล์ greeting.txt ดังนี้
```
Hello frogconn! You are 25
```
>***frogconn = ชื่อจากระบบ


กลับที่ไฟล์ notes.js และเพิ่มโค้ดดังนี้

 ```js
 console.log('Starting notes.js');

 module.exports.addNote = ()=>{
   console.log('addNote')
   return 'New note';
 };
 ```
 กลับที่ไฟล์ app.js และเพิ่มโค้ดดังนี้

 ```js
console.log('Starting app.js');

const fs = require('fs');
const os = require('os');
const notes = require('./notes.js');

var res = notes.addNote()
console.log(res)
```
ทดลองรันโปรแกรม หากไม่เกิดข้อผิดพลาดจะได้ผลลัพธ์ ที่อยู่ในไฟล์ greeting.txt ดังนี้

```
Starting app.js
Staring notes.js
addNote
New note
```


กลับที่ไฟล์ notes.js และเพิ่มโค้ดดังนี้

```js
console.log('Staring notes.js');

module.exports.addNote = () => {
    console.log('addNote');

    return 'New note'
}

module.exports.add = (a, b) => {
    return a + b;
}

 ```
 กลับที่ไฟล์ app.js และเพิ่มโค้ดดังนี้

 ```js
console.log('Starting app.js');

const fs = require('fs');
const os = require('os');
const notes = require('./notes.js');

console.log('Result:',notes.add(9,-2))
```
ทดลองรันโปรแกรม หากไม่เกิดข้อผิดพลาดจะได้ผลลัพธ์ ที่อยู่ในไฟล์ greeting.txt ดังนี้

```
Starting app.js
Staring notes.js
Result: 7
```
## Using 3rd Party Modules

```
npm -v
```

```
npm init
```

```
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help json` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (lab)

```

```
It only covers the most common items, and tries to guess sensible defaults.

See `npm help json` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (lab)
version: (1.0.0)
description:
entry point: (app.js)
test command:
git repository:
keywords:
author:
license: (ISC)
About to write to /Applications/MAMP/htdocs/kku/course_nodejs/lab/package.json:

{
  "name": "lab",
  "version": "1.0.0",
  "description": "",
  "main": "app.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}


Is this OK? (yes) yes
```

จากนั้นจะมีไฟล์ `package.json` เพิ่มขึ้นมา

```
{
  "name": "lab",
  "version": "1.0.0",
  "description": "",
  "main": "app.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}

```

ในส่วนนี้เราจะทดลองใช้ 3rd Party Modules ชื่อ `lodash` โดยเราสามารถเริ่มใช้งานได้โดยไปที่ https://npmjs.com และค้นหา package ชื่อ lodash

![](images/2018-06-12-16-14-40.png#center)

จากนั้นกลับมาที่ Terminal และเริ่มต้น Install module ด้วยคำสั่งดังนี้

```
npm install lodash --save
```
จากนั้นระบบจะทำการติดตั้ง Module ให้โดยแสดงผลลัพธ์ดังนี้

```
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN lab@1.0.0 No description
npm WARN lab@1.0.0 No repository field.

+ lodash@4.17.10
added 1 package from 2 contributors and audited 1 package in 1.693s
found 0 vulnerabilities

```

ลองตรวจสอบว่า lodash มีอะไรให้เราใช้งานได้บ้างที่เว็บ https://lodash.com ให้ทำการเพิ่มโค้ดที่ไฟล์ app.js ดังนี้
```js
console.log('Starting app.js');

const fs = require('fs');
const os = require('os');
const _ = require('lodash');
const notes = require('./notes.js');

console.log(_.isString(true))
console.log(_.isString('Suchart'))
```

ทดลองรันโปรแกรม
```
Starting app.js
Staring notes.js
false
true
```

ทดลองใช้ function อื่นๆ เช่น `uniq`
```js
console.log('Starting app.js');

const fs = require('fs');
const os = require('os');
const _ = require('lodash');
const notes = require('./notes.js');

// console.log(_.isString(true))
// console.log(_.isString('Suchart'))
var filteredArray = _.uniq(['Suchart', 1, 'Suchart', 1, 2, 3, 4])
console.log(filteredArray)
```
 ​
ทดลองรันโปรแกรม
```
Starting app.js
Staring notes.js
[ 'Suchart', 1, 2, 3, 4 ]
```

>ทดลองทำการลบ Directory node_modules และทำการ install เพื่อดูผลลัพธ์
## Restarting App with Nodemon

ค้นหาและดูราลละเอียด Modules ที่ http://www.npmjs.com

![](images/2018-06-12-17-40-25.png#center)

ทำการติดตั้งด้วยคำสั่ง
```
npm install nodemon -g
```

หากไม่มีข้อผิดพลาดจะแสดงผลลัพธ์ ดังภาพด้านล่าง

![](images/2018-06-12-17-44-57.png#center)

จากนั้นให้ทำการรันโปรแกรมด้วยคำสั่ง

```
nodemon app.js
```

ผลการรันโปรแกรม
```
[nodemon] 1.17.5
[nodemon] to restart at any time, enter `rs`
[nodemon] watching: *.*
[nodemon] starting `node app.js`
Starting app.js
Staring notes.js
[ 'Suchart', 1, 2, 3, 4 ]
[nodemon] clean exit - waiting for changes before restart
```

ทำการแก้ไข Code ที่ไฟล์ app.js ดังนี้
```js
console.log('Starting app.js');

const fs = require('fs');
const os = require('os');
const _ = require('lodash');
const notes = require('./notes.js');

// console.log(_.isString(true))
// console.log(_.isString('Suchart'))
var filteredArray = _.uniq(['Mike'])
console.log(filteredArray)
```
จากนั้นให้ทำการ Save ไฟล์ nodemon จะช่วย Restart app.js ให้โดยอัตโนมัติ
```
[nodemon] restarting due to changes...
[nodemon] starting `node app.js`
Starting app.js
Staring notes.js
[ 'Mike' ]
[nodemon] clean exit - waiting for changes before restart
```

>เราสามารถออกจาก Mode การรันของ nodemon ได้โดยการกดปุ่ม Ctrl+c

## Workshop สร้างเว็บแอปพลิเคชันเพื่อบริการ Static File

1. สร้างไฟล์ server.js ที่ C:\nodejs\lab2

![](images/2018-06-14-07-50-17.png#center)

2. ทำการดาวน์โหลดไฟล์รูปภาพที่ต้องการมาเก็บไว้ที่ C:\nodejs\lab2\file_server
3. ทำการรันโปรแกรมด้วยคำสั่ง
```
 node server.js
```
4. จากนั้นทดลองเข้าถึงไฟล์ผ่านเว็บเบราว์เซอร์ เพื่อเข้าถึงรูปภาพเช่น
```
http://localhost:4000/Donald-Trump.jpg
```

5. หากไม่เกิดข้อผิดพลาดจะสามารถเข้าถึงไฟล์ได้ เช่น
![](images/2018-06-14-07-52-40.png#center)


## Workshop เพิ่มความปลอดภัยให้เว็บแอปพลิเคชันที่ให้บริการ Static File ด้วย HashIds
![](images/2018-06-14-07-57-02.png#center)
1. ติดตั้ง โมดูล HashIds (https://www.npmjs.com/package/hashids) ด้วยคำสั่ง
```
npm install --save hashids
```
2. แก้ไขโค้ดที่ไฟล์  server.js
![](images/2018-06-14-07-55-22.png#center)

3. ทดลองรันโปรแกรม
```
node server.js
```
4. ตรวจสอบผลลัพธ์
![](images/2018-06-14-07-57-29.png#center)

***Note
กรณีที่ต้องการได้ซึ่งข้อความที่มีการเข้ารหัส สามารถทำได้ดังนี้
```
var Hashids = require('hashids');
var hashids = new Hashids('XYz', 10, 'abcdefghijklmnopqrstuvwxyz');
var id = hashids.encodeHex('001');
console.log(id);

หรือหากต้องการเป็นตัวอักษร สามารถทำได้ดังนี้
var Hashids = require('hashids');
var hashids = new Hashids('XYz', 10, 'abcdefghijklmnopqrstuvwxyz');
var hex = Buffer('Hello World').toString('hex');
console.log (hex);

var encoded = hashids.encodeHex(hex);
console.log (encoded);

var decodedHex = hashids.decodeHex(encoded);
console.log (decodedHex);

var string = Buffer(decodedHex, 'hex').toString('utf8');
console.log (string);

```

## Workshop สร้าง RESTFul API ด้วย Express.js
![](images/2018-06-14-08-10-55.png#center)
1. สร้างโปรเจ็คสามารถสร้างโดยวิธีการ Manual โดยทำการสร้างไฟล์ชื่อ package.json หรือจะใช้คำสั่ง `npm init` ในการสร้างก็ได้ โดยตามตัวอย่างนี้จะใช้วิธี npm init
```
{
  "name": "express-nodejs",
  "version": "1.0.0",
  "description": "Restful Node.js with Express",
  "main": "index.js"
}

```
2. ติดตั้ง express ด้วยคำสั่ง
```
 npm install express --save
```
เพิ่มโค้ดที่ไฟล์ index.js

3. เพิ่มโค้ดที่ไฟล์ index.js
![](images/2018-06-14-08-00-21.png#center)

4. สั่งให้ Server เริ่มทำงานด้วยคำสั่ง
```
node index.js
```
5. ทำการจำลองการสร้าง RESTFul API
```
GET localhost:3000/
GET localhost:3000/user
GET localhost:3000/user/:id
POST localhost:3000/user
```
6. ทำการสร้างไฟล์ users.js และเพิ่มโค้ด
![](images/2018-06-14-08-02-24.png#center)

7. เพิ่มการเรียกใช้งาน user ในไฟล์ index.js
```
var users = require('./users');
```
8. ทำการเพิ่ม route ดังนี้
![](images/2018-06-14-08-03-30.png#center)
9. ทำการทดสอบด้วย Postman
![](images/2018-06-14-08-04-06.png#center)
10. ทดสอบทำการ Post ข้อมูล
![](images/2018-06-14-08-04-49.png#center)
11. เนื่องจากระบบยังไม่สามารถ Parser body ได้ จึงจำเป็นต้องติดตั้งโมดูลเพิ่ม
```
npm install body-parser --save
```
12. จากนั้นทำการเพิ่มโค้ด
![](images/2018-06-14-08-05-53.png#center)
13. ทำการทดสอบ Post ข้อมูลอีกครั้ง
![](images/2018-06-14-08-06-25.png#center)
14. จะพบว่าระบบสามารถรับข้อมูลที่เป็นการ Post ได้
15. เพิ่มความปลอดภัยโดยการตรวจ Token จาก Header
![](images/2018-06-14-08-08-45.png#center)

## วิธีการทำ NodeJS แยก config ระหว่าง dev กับ production

ปกติถ้าเราใช้ NodeJS ในการพัฒนา REST Api แล้วคงหนีไม่พ้นที่ต้องมีการตั้งค่า Config ระบบต่างๆ ใส่ใน file เอาไว้ ที่นี้ปัญหาที่พบบ่อยก็คือลืมเปลี่ยน ค่า config ใน environment ต่างๆ เช่น Test, Productionสำหรับ NodeJs เรามี lib อยู่ตัวนึงที่แนะนำคือ config โดยการติดตั้งผ่านคำสั่ง npm ดังนี้

```
npm install config --save
```

เมื่อติดตั้งเสร็จแล้วให้สร้าง folder ชื่อ config ใน project ก่อนดังภาพ

![](images/2018-06-11-17-15-14.png#center)

ตัว lib config นี้จะอ่านค่าว่าเราจะใช้ file ชื่ออะไรจาก NODE_ENV แต่ถ้าในกรณีที่ไม่ได้กำหนดไว้ก็จะไปหา file ชื่อ default.json ใน folder configใน file config สามารถใส่ในรูปแบบ json ได้เลยดังตัวอย่างดังนี้

```
// config/default.json
{
   "vat" : 7
}
// config/production.json
{
   "vat" : 10
}
```

ตอนเรียกใช้งานใน nodejs เราสามารถเรียกจากชื่อได้เลยดังนี้

```js
// app.js
const config = require('config');
let vat = config.get('vat');
console.log(vat);
```

หลังจากนั้นให้ทดลอง start nodejs ดูด้วยคำสั่งดังนี้

```
node app.js
// จะไปอ่าน file ที่ /config/default.json
ผลลัพธ์จะได้เป็น 7

NODE_ENV=production node app.js
// จะไปอ่าน file ที่ /config/production.json
ผลลัพธ์จะได้เป็น 10
```
