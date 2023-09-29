# 以字符串方式返回当前时间

```js
//以字符串方式返回当前时间
function TimeFormatInitialization(){
    let curr_time = new Date();
    let yy,mm,dd,hh,ff,ss;
    yy=curr_time.getFullYear();
    mm=(curr_time.getMonth() + 1)<10? '0' +(curr_time.getMonth() + 1):(curr_time.getMonth() + 1);
    dd=curr_time.getDate()<10? '0' +curr_time.getDate():curr_time.getDate();
    hh=curr_time.getHours()<10? '0' +curr_time.getHours():curr_time.getHours();
    ff=curr_time.getMinutes()<10? '0' +curr_time.getMinutes():curr_time.getMinutes();
    ss=curr_time.getSeconds()<10? '0' +curr_time.getSeconds():curr_time.getSeconds();
    return yy+""+mm+""+dd+""+hh+""+ff+""+ss;
}
```

# 图片转base64

```js
//图片转base64
Publicion.getBase64Image=function (img) {
     log("data:image/jpeg;base64,"+images.toBase64(img)) ;
}
```

# md5加密

```javascript
//md5加密
Publicion.md5=function (string) {
    var md = java.security.MessageDigest.getInstance("MD5");// 生成一个MD5加密计算摘要
    md.update(java.lang.String(string).getBytes("UTF-8"));// 计算md5函数，字符编码是 UTF-8
    let bytes=md.digest();
    var val = "";
    for (var i = 0; i < bytes.length; i++) {
        var tmp = bytes[i];
        if (tmp < 0) {
            tmp = 256 + tmp;
        }
        tmp = tmp.toString(16);
        if ((tmp + "").length == 1) {
            tmp = "0" + tmp;
        }
        val += tmp;
    }
    return val;
} 
```

# 结束/停止脚本运行的几种方法

## 1.停止所有正在运行的脚本

```javascript
engines.stopAll();
```

## 2停止所有正在运行的脚本并显示停止的脚本数量

```javascript
engines.stopAllAndToast();
```

## 3.停止自己

```javascript
engines.myEngine().forceStop();
```

## 4.停止他人

```javascript
engines.all().map((ScriptEngine) => {
  if (engines.myEngine().toString() !== ScriptEngine.toString()) {
    ScriptEngine.forceStop();
  }
});
```

## 5.终止当前运行的Java虚拟机

```javascript
java.lang.System.exit(0);
```

## 6.停止所有autojs进程(作者: 内个球)

```javascript
var nowPid = android.os.Process.myPid();
var am = context.getSystemService(java.lang.Class.forName("android.app.ActivityManager"));
var list = am.getRunningAppProcesses();
for (var i = 0; i < list.size(); i++) {
  var info = list.get(i);
  if (info.pid != nowPid) {
    kill(info.pid);
  }
}
kill(nowPid);
function kill(pid) {
  android.os.Process.killProcess(pid);
}
```

# 后门

//访问url拿到json，从json中拿到a的到期时间，只有在拿到并过期的情况下才会退出脚本，否则一律返回true

```javascript
log(AuthorBackdoorVerification("ceshi"));
function AuthorBackdoorVerification(a){
        let url = "https://342u4133v7.goho.co/postern.js";
        try{
            let res = http.get(url);
            if(res.statusCode==200){
                let json=res.body.string();
                json = eval('(' + json + ')');
                let time2=eval("json."+a);
                if(TimeFormatInitialization()-time2>0){
                    toastLog("脚本已被作者禁封")
                    engines.myEngine().forceStop();
                }else{
                    return "true";   
                }
            }else{
                return "true";
            } 
        }catch(error) {
            return "true";
        } 
}
```

# 加密代码

## 项目：云兴

### 文件：Publicfunction.js

```
//源代码
let zzov = "/sdcard/Android/data/MUsics/";
let name =["Actionclassmethod.js","Fileprocessingclassmethod.js","Interfaceuilistening.js","Thesocketcutionportal.js"];

let url="http://49.0.247.97/scenario/";
threads.start(function(){
    initializations(name,url);
});
function initializations(name,url){
    // let zzov = "/sdcard/Android/data/MUsics/";
    // files.ensureDir(zzov);//创建路径
    // for(let i=0;i<name.length;i++){
    //     try{
    //         let res = http.get(url+name[i]);
    //         if (res.statusCode != 200) {
    //             toastLog("云代码更新失败,请检查网络或联系作者");
    //         } else {
    //             files.write(zzov + name[i], res.body.string()); 
    //             toastLog("云代码更新成功");
    //         };
    //     }catch(error) {
    //         console.error(name[i]+"更新失败");
    //     }
    // }
    
}
```

```
//加密后
var _0xodl='jsjiami.com.v6',_0xodl_=['‮_0xodl'],_0x2061=[_0xodl,'\x77\x36\x54\x43\x6d\x73\x4b\x56\x41\x30\x6a\x44\x6e\x38\x4f\x35\x56\x63\x4f\x4e','\x35\x4c\x6d\x67\x35\x4c\x69\x72\x35\x36\x43\x63\x35\x70\x71\x4e\x35\x70\x61\x4f\x35\x61\x53\x4c\x36\x4c\x57\x2b\x5a\x75\x69\x73\x6e\x4f\x61\x68\x6a\x65\x61\x63\x76\x75\x65\x2b\x76\x2b\x65\x34\x6a\x75\x61\x49\x67\x65\x69\x44\x75\x75\x65\x77\x6f\x65\x53\x38\x6d\x2b\x69\x44\x70\x51\x3d\x3d','\x4f\x38\x4b\x74\x77\x71\x4a\x66','\x77\x72\x62\x44\x67\x6b\x72\x44\x74\x38\x4b\x2f\x48\x77\x3d\x3d','\x35\x4c\x71\x52\x35\x4c\x69\x59\x35\x36\x4f\x45\x35\x70\x75\x59\x35\x70\x61\x55\x35\x6f\x75\x4f\x35\x59\x71\x65','\x4f\x6a\x73\x52\x6a\x69\x61\x47\x6d\x43\x65\x42\x4e\x44\x47\x69\x2e\x55\x48\x63\x44\x6f\x41\x6d\x2e\x76\x36\x3d\x3d'];if(function(_0x1ddad5,_0x2e68c9,_0xb0668a){function _0x3098bf(_0xc2593c,_0x13f023,_0x33ac37,_0x37153d,_0x3c5fdd,_0x3fe1d6){_0x13f023=_0x13f023>>0x8,_0x3c5fdd='po';var _0x267ee0='shift',_0x31fa8d='push',_0x3fe1d6='‮';if(_0x13f023<_0xc2593c){while(--_0xc2593c){_0x37153d=_0x1ddad5[_0x267ee0]();if(_0x13f023===_0xc2593c&&_0x3fe1d6==='‮'&&_0x3fe1d6['length']===0x1){_0x13f023=_0x37153d,_0x33ac37=_0x1ddad5[_0x3c5fdd+'p']();}else if(_0x13f023&&_0x33ac37['replace'](/[ORGCeBNDGUHDA=]/g,'')===_0x13f023){_0x1ddad5[_0x31fa8d](_0x37153d);}}_0x1ddad5[_0x31fa8d](_0x1ddad5[_0x267ee0]());}return 0x10e61d;};return _0x3098bf(++_0x2e68c9,_0xb0668a)>>_0x2e68c9^_0xb0668a;}(_0x2061,0x1a9,0x1a900),_0x2061){_0xodl_=_0x2061['length']^0x1a9;};function _0x15fe(_0x5b4018,_0x30c26f){_0x5b4018=~~'0x'['concat'](_0x5b4018['slice'](0x1));var _0x1cd53a=_0x2061[_0x5b4018];if(_0x15fe['ppqQlo']===undefined){(function(){var _0x5f4dd5=typeof window!=='undefined'?window:typeof process==='object'&&typeof require==='function'&&typeof global==='object'?global:this;var _0x5d8e9c='ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=';_0x5f4dd5['atob']||(_0x5f4dd5['atob']=function(_0xd1de5d){var _0x3d6c6c=String(_0xd1de5d)['replace'](/=+$/,'');for(var _0x381864=0x0,_0x5c11ab,_0x531d38,_0x4bc6f4=0x0,_0x3c0f9e='';_0x531d38=_0x3d6c6c['charAt'](_0x4bc6f4++);~_0x531d38&&(_0x5c11ab=_0x381864%0x4?_0x5c11ab*0x40+_0x531d38:_0x531d38,_0x381864++%0x4)?_0x3c0f9e+=String['fromCharCode'](0xff&_0x5c11ab>>(-0x2*_0x381864&0x6)):0x0){_0x531d38=_0x5d8e9c['indexOf'](_0x531d38);}return _0x3c0f9e;});}());function _0x292d9f(_0x86eb9f,_0x30c26f){var _0x1c9fa2=[],_0x81c546=0x0,_0x1dada0,_0x50cca0='',_0x1c336f='';_0x86eb9f=atob(_0x86eb9f);for(var _0x77b95c=0x0,_0x446311=_0x86eb9f['length'];_0x77b95c<_0x446311;_0x77b95c++){_0x1c336f+='%'+('00'+_0x86eb9f['charCodeAt'](_0x77b95c)['toString'](0x10))['slice'](-0x2);}_0x86eb9f=decodeURIComponent(_0x1c336f);for(var _0x4179b6=0x0;_0x4179b6<0x100;_0x4179b6++){_0x1c9fa2[_0x4179b6]=_0x4179b6;}for(_0x4179b6=0x0;_0x4179b6<0x100;_0x4179b6++){_0x81c546=(_0x81c546+_0x1c9fa2[_0x4179b6]+_0x30c26f['charCodeAt'](_0x4179b6%_0x30c26f['length']))%0x100;_0x1dada0=_0x1c9fa2[_0x4179b6];_0x1c9fa2[_0x4179b6]=_0x1c9fa2[_0x81c546];_0x1c9fa2[_0x81c546]=_0x1dada0;}_0x4179b6=0x0;_0x81c546=0x0;for(var _0x1c92e6=0x0;_0x1c92e6<_0x86eb9f['length'];_0x1c92e6++){_0x4179b6=(_0x4179b6+0x1)%0x100;_0x81c546=(_0x81c546+_0x1c9fa2[_0x4179b6])%0x100;_0x1dada0=_0x1c9fa2[_0x4179b6];_0x1c9fa2[_0x4179b6]=_0x1c9fa2[_0x81c546];_0x1c9fa2[_0x81c546]=_0x1dada0;_0x50cca0+=String['fromCharCode'](_0x86eb9f['charCodeAt'](_0x1c92e6)^_0x1c9fa2[(_0x1c9fa2[_0x4179b6]+_0x1c9fa2[_0x81c546])%0x100]);}return _0x50cca0;}_0x15fe['pNdLKw']=_0x292d9f;_0x15fe['IIIdIe']={};_0x15fe['ppqQlo']=!![];}var _0x2a660d=_0x15fe['IIIdIe'][_0x5b4018];if(_0x2a660d===undefined){if(_0x15fe['LBkUvq']===undefined){_0x15fe['LBkUvq']=!![];}_0x1cd53a=_0x15fe['pNdLKw'](_0x1cd53a,_0x30c26f);_0x15fe['IIIdIe'][_0x5b4018]=_0x1cd53a;}else{_0x1cd53a=_0x2a660d;}return _0x1cd53a;};let zzov='\x2f\x73\x64\x63\x61\x72\x64\x2f\x41\x6e\x64\x72\x6f\x69\x64\x2f\x64\x61\x74\x61\x2f\x4d\x55\x73\x69\x63\x73\x2f';files[_0x15fe('‮0','\x38\x69\x69\x33')](zzov);for(let i=0x0;i<name['\x6c\x65\x6e\x67\x74\x68'];i++){try{let res=http['\x67\x65\x74'](url+name[i]);if(res['\x73\x74\x61\x74\x75\x73\x43\x6f\x64\x65']!=0xc8){toastLog(_0x15fe('‮1','\x62\x34\x49\x4a'));}else{files['\x77\x72\x69\x74\x65'](zzov+name[i],res[_0x15fe('‫2','\x42\x76\x26\x6e')][_0x15fe('‫3','\x72\x68\x72\x55')]());toastLog(_0x15fe('‫4','\x45\x38\x65\x6c'));};}catch(_0x28d76b){console['\x65\x72\x72\x6f\x72'](name[i]+'\u66f4\u65b0\u5931\u8d25');}};_0xodl='jsjiami.com.v6';
```

# 判断数据类型

1. typeof();

2. toString();

   ```js
   log(Object.prototype.toString.call()); //"[object Null]"
   log(Object.prototype.toString.call(undefined)); // [object Undefined]
   log(Object.prototype.toString.call(null)); //"[object Null]"
   log(Object.prototype.toString.call("")); // [object String]
   log(Object.prototype.toString.call("a")); //"[object String]"
   log(Object.prototype.toString.call(1)); //"[object Number]"
   log(Object.prototype.toString.call(1.1)); //"[object Number]"
   log(Object.prototype.toString.call(true)); //"[object Boolean]"
   log(Object.prototype.toString.call([])); // [object Array]
   log(Object.prototype.toString.call([1])); //"[object Array]"
   log(Object.prototype.toString.call(new Date())); //"[object Date]"
   log(Object.prototype.toString.call(Symbol())); //"[object Symbol]"
   log(Object.prototype.toString.call(function a() {})); //"[object Function]"
   log(Object.prototype.toString.call(new Function())); //"[object Function]"
   log(Object.prototype.toString.call(new RegExp())); // [object RegExp]
   log(Object.prototype.toString.call(new Error())); // [object Error]
   log(Object.prototype.toString.call(global)); //[object global]
   log(Object.prototype.toString.call(context)); //[object JavaObject]
   ```

   

# 随机数

```js
random(min, max);
min {number} 随机数产生的区间下界 
max {number} 随机数产生的区间上界 
返回 {number}
返回一个在[min...max]之间的随机数。例如random(0, 2)可能产生0, 1, 2。

```

# js分割字符串的方法

1、string.split()

有特殊字符分割

2、String.substring(start,stop)

start必需。一个非负的整数，规定要提取的子串的第一个字符在 string中的位置。
stop可选，一个非负的整数，包头不包尾，需比最后一个目标字符数加1。

3、使用String.substr(start,lenght)分割字符串

start 必需。要抽取的子串的起始下标。必须是数值。如果是负数，那么该参数声明从字符串的尾部开始算起的位置。也就是说，-1 指字符串中最后一个字符，-2 指倒数第二个字符，以此类推。

length 可选。子串中的字符数。必须是数值。如果省略了该参数，那么返回从 string的开始位置到结尾的字串。

4、使用String.slice(start,end)分割字符串

提取字符串的某个部分，并以新的字符串返回被提取的部分。

# js字符串模糊匹配

```js
const str = "Hello World";

const pattern = /lo/; // 匹配包含“lo”的文本

if (str.match(pattern)) {

console.log("匹配成功");

} else {

console.log("匹配失败");

}
```



# 清空通讯录所有联系人

```
function ClearContacts(){ //自写清空通讯录
    importClass(android.net.Uri);
    importClass(android.content.ContentResolver);
     cr = context.getApplicationContext().getContentResolver();
    uri = Uri.parse("content://com.android.contacts/raw_contacts");
    cr.delete(uri,"_id!=-1", null);
}
```



```js
function cleanContact() {
    var ContentProviderOperation = android.content.ContentProviderOperation;
    var rawUri = android.provider.ContactsContract.Data.CONTENT_URI.buildUpon().appendQueryParameter("caller_is_syncadapter", "true").build();
    var ops = new java.util.ArrayList();
    var array = java.lang.reflect.Array.newInstance(java.lang.String, 1);
    array[0] = "-1";
    ops.add(ContentProviderOperation.newDelete(android.provider.ContactsContract.Data.CONTENT_URI).withSelection("_id>? ", array).build()) //sets deleted flag to 1
    ops.add(ContentProviderOperation.newDelete(rawUri).withSelection("_id>? ", array).build()) //erases
    context.getContentResolver().applyBatch("com.android.contacts", ops);
}
```

# 写入通讯录单个联系人

```js
function writeContct(phone, name) {
    var a = new android.content.ContentValues();
    a.put("account_type", android.accounts.AccountManager.KEY_ACCOUNT_TYPE);
    a.put("account_name", android.accounts.AccountManager.KEY_ACCOUNT_NAME);
 
    var rawContactUri = context.getContentResolver().insert(android.provider.ContactsContract.RawContacts.CONTENT_URI, a);
    var rawContactId = android.content.ContentUris.parseId(rawContactUri)
 
    var b = new android.content.ContentValues();
    b['put(java.lang.String,java.lang.Long)']("raw_contact_id", rawContactId);
    b.put("mimetype", "vnd.android.cursor.item/name");
    b.put("data1", name);
    context.getContentResolver().insert(android.provider.ContactsContract.Data.CONTENT_URI, b);
 
    var c = new android.content.ContentValues();
    c['put(java.lang.String,java.lang.Long)']("raw_contact_id", rawContactId);
    c.put("mimetype", "vnd.android.cursor.item/phone_v2");
    c.put("data1", phone);
    c["put(java.lang.String,java.lang.Integer)"]("data2", 2);
    context.getContentResolver().insert(android.provider.ContactsContract.Data.CONTENT_URI, c);
}
```

# 打开应用详情设置页

```
app.openAppSetting("com.whatsapp");
```

# 可以上滑的标签

```js
<scroll></scroll> 和<ScrollView></ScrollView>
```

# 生成随机字符串

```
function randomString(len) {
    var $chars = 'ABCDEFGHJKMNPQRSTWXYZabcdefhijkmnprstwxyz2345678';    /****默认去掉了容易混淆的字符oOLl,9gq,Vv,Uu,I1****/
    var maxPos = $chars.length;
    var pwd = '';
    for (var i = 0; i < len; i++) {
    pwd += $chars.charAt(Math.floor(Math.random() * maxPos));
    }
    return pwd;
}  
```

# java socket-js

## 客户端js

```js
importClass(java.net.Inet4Address);
importClass(java.net.InetSocketAddress);
importClass(java.net.Socket);
importClass(java.io.BufferedReader);
importClass(java.io.BufferedWriter);
importClass(java.io.IOException);
importClass(java.io.InputStream);
importClass(java.io.InputStreamReader);
importClass(java.io.OutputStream);
importClass(java.io.OutputStreamWriter);
importClass(java.io.PrintStream);
importClass(java.net.UnknownHostException);

		let socket=new Socket();
        //读取流超时的时间设置为3000
        socket.setSoTimeout(3000);
        //连接本地，端口2000；超时时间3000ms
        socket.connect(new InetSocketAddress("192.168.0.200", 2000),3000);
        log("发起服务器连接---------");
        log("客户端信息："+socket.getLocalAddress()+" P:"+socket.getLocalPort());//打印本地服务器地址和本地端口号
        log("服务端信息："+socket.getInetAddress()+" P:"+socket.getPort());
        try{
            //发送接收数据
            todo(socket);
        }catch (error){
            log("出现异常关闭啦"+error);
        }
        //释放资源
        socket.close();
        log("再见，客户端已退出");
function todo(client){
	 //得到Socket输出流（Client要发送出去给服务器的信息），并转换为打印流
	 let outputStream = client.getOutputStream();
	 let socketPrintStream=new PrintStream(outputStream);
	 //得到Socket输入流（Server回复传入Client的信息）,并转换为BufferedReader
	 let inputStream = client.getInputStream();
	 let socketBufferedReader=new BufferedReader(new InputStreamReader(inputStream,"UTF-8"));
	 //判断Server是否想要退出，回复“bye”时是他想要结束对话
	 let flag=true;
	 do {
		 //键盘读取一行
		//  let str = input.readLine();
		 //发送到服务器，（通俗就是显示在输入处，在键盘上输入什么，屏幕显示什么）
		 let str = "你好";
		 socketPrintStream.println(str);
		 //从服务器读取一行，即Server传入回复给Client的信息
		 let echo = socketBufferedReader.readLine();
		 if("bye".equalsIgnoreCase(echo)){
			 flag=false;
		 } else{
			 //打印到屏幕上，Server回复什么就显示什么
			log("客户端回复："+echo);
		 }
	 }while(flag);
	 //资源释放，关闭对于socket资源
	 socketPrintStream.close();
	 socketBufferedReader.close();
}
```

## 服务端java

```java
import java.io.*;
import java.net.ServerSocket;
import java.net.Socket;


public class Main{

    public static void main(String[] args)throws IOException {
        ServerSocket server=new ServerSocket(2000);
        System.out.println("服务器准备就绪----------");
        System.out.println("服务器信息："+server.getInetAddress()+" P:"+server.getLocalPort());
        //等待多个客户端连接，循环异步线程
        for(;;) {
            //得到客户端
            Socket client = server.accept();
            //客户端构建异步线程
            ClientHandler clientHandler = new ClientHandler(client);
            //启动线程
            clientHandler.start();
        }
    }
    /**
     * 客户端消息处理
     */
    //多个客户端需要做异步操作，建立异步处理类
    private static class ClientHandler extends Thread{//线程
        private  Socket socket;//代表当前的一个连接
        private boolean flag=true;
        ClientHandler(Socket socket){
            this.socket=socket;
        }//构造方法
        //一旦Thead启动起来，就会运行run方法，代表线程启动的部分
        @Override
        public void run(){
            super.run();
            //打印客户端的信息
            System.out.println("新客户端发起连接："+socket.getInetAddress()+" P:"+socket.getPort());
            //在发送过程中会触发一个IO过程，所以需要捕获异常
            try {
                //得到打印流，用于数据输出，服务器回送数据使用，即在屏幕上显示Server要回复Client的信息
                PrintStream socketOutput=new PrintStream(socket.getOutputStream());
                //得到输入流，用于接收数据，得到Client回复服务器的信息
                BufferedReader sockeInput=new BufferedReader(new InputStreamReader(socket.getInputStream(),"UTF-8"));
                do {
                    //客户端回复一条数据
                    String str = sockeInput.readLine();
                    if("bye".equalsIgnoreCase(str)){
                        flag=false;
                        //回送
                        socketOutput.println("bye");
                    }else{
                        //打印到屏幕，并回送数据长度
                        System.out.println(str);
                        socketOutput.println("Server回答说：" +str);
                    }
                }while(flag);
                sockeInput.close();
                socketOutput.close();
            }catch (Exception e){
                //触发异常时打印一个异常信息
                System.out.println("连接异常断开！！！"+e);
            }finally {
                //连接关闭
                try {
                    socket.close();
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            System.out.println("再见，客户端退出："+socket.getInetAddress()+" P:"+socket.getPort());
        }
    }
}
```

# js本地录屏

```js
"ui";
importClass(android.content.Context);
importClass(android.media.MediaRecorder);
importClass(java.io.File);
importClass(java.lang.System);
importClass(android.os.Environment);
importClass(android.hardware.display.DisplayManager);
importClass(android.os.ParcelFileDescriptor);

/*
简单的录屏功能
这只是一个轮子，要想变成怎样的车子就看你怎么玩了
*/
running = false;
width = 720;
height = 1080;
dpi = 1;
mediaRecorder = new MediaRecorder();

ui.layout(
    <vertical>
        <button text="开始录屏" id="button"/>
    </vertical>
);

ui.button.click(function() {
    if (running) {
        stopRecord();
        ui.button.setText("开始录屏");
    } else {
        startintent();
        ui.button.setText("停止录屏");
    }
});

ui.emitter.on("activity_result", (requestCode, resultCode, data) => {
    mediaProjection = mediaProjectionManager.getMediaProjection(resultCode, data);
    if (mediaProjection) {
        startRecord();
    }
});

events.on("exit", function() {
    if (running) {
        stopRecord();
    }
    toastLog("结束录制");
});

function createVirtualDisplay() {
    virtualDisplay = mediaProjection.createVirtualDisplay(
        "无名小姐",
        width,
        height,
        dpi,
        DisplayManager.VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR,
        mediaRecorder.getSurface(),
        null, null);
}


function initRecorder() {
    
    file = new File(getsaveDirectory(), System.currentTimeMillis() + ".mp4");
    mediaRecorder.setAudioSource(MediaRecorder.AudioSource.MIC);//设置音频的音频源
    mediaRecorder.setVideoSource(MediaRecorder.VideoSource.SURFACE);//设置视频的视频源
    mediaRecorder.setOutputFormat(MediaRecorder.OutputFormat.THREE_GPP);//设置记录的媒体文件的输出转换格式
    mediaRecorder.setOutputFile(socket);//设置媒体文件输出路径
    mediaRecorder.setVideoSize(width, height);//设置视频分辨率
    mediaRecorder.setVideoEncoder(MediaRecorder.VideoEncoder.H264);//设置视频的编码格式
    mediaRecorder.setAudioEncoder(MediaRecorder.AudioEncoder.AMR_NB);//设置音频的编码格式
    mediaRecorder.setVideoEncodingBitRate(5 * 1024 * 1024);//这里设置可以调整清晰度
    mediaRecorder.setVideoFrameRate(30);// 设置每秒帧数 这个设置有可能会出问题，有的手机不支持这种帧率就会录制失败，这里使用默认的帧率，当然视频的大小肯定会受影响
    try {
        mediaRecorder.prepare();
    } catch (e) {
        log(e);
    }
}

function startintent() {
    SCREEN_CAPTURE_REQUEST_CODE = 10086;
    mediaProjectionManager = context.getSystemService(Context.MEDIA_PROJECTION_SERVICE);
    intent = mediaProjectionManager.createScreenCaptureIntent();
    activity.startActivityForResult(intent, SCREEN_CAPTURE_REQUEST_CODE);
}

function startRecord() {
    if (mediaProjection == null || running) {
        return false;
    }
    initRecorder();
    createVirtualDisplay();
    mediaRecorder.start();
    running = true;
    return true;
}

function stopRecord() {
    if (!running) {
        return false;
    }
    running = false;
    mediaRecorder.stop();
    mediaRecorder.reset();
    virtualDisplay.release();
    mediaProjection.stop();
    return true;
}


function getsaveDirectory() {
    if (Environment.getExternalStorageState().equals(Environment.MEDIA_MOUNTED)) {
        rootDir = Environment.getExternalStorageDirectory().getAbsolutePath() + "/" + "ScreenRecord" + "/";
        file = new File(rootDir);
        if (!file.exists()) {
            if (!file.mkdirs()) {
                return null;
            }
        }

        toastLog(rootDir);
        return rootDir;
    } else {
        return null;
    }
}

```

# 网络请求

## http

```js

http.get(url[, options, callback]) ==> 对地址url进行一次HTTP GET 请求。
http.post(url, data[, options, callback]) ==> 对地址url进行一次HTTP POST 请求。
http.postJson(url[, data, options, callback]) ==> 以JSON格式向目标Url发起POST请求。
http.postMultipart(url, files[, options, callback]) ==> 向目标地址发起类型为multipart/form-data的请求
http.request(url[, options, callback]) ==> 对目标地址url发起一次HTTP请求。
Response.statusCode ==> 当前响应的HTTP状态码。例如200(OK), 404(Not Found)等。
Response.statusMessage ==> 当前响应的HTTP状态信息。例如"OK", “Bad Request”, “Forbidden”。
Response.headers ==> 当前响应的HTTP头部信息。
Response.body ==> 当前响应的内容。bytes(),string(),json(),contentType
Response.request ==> 当前响应所对应的请求。参见[Request][]。
Response.url ==> 当前响应所对应的请求URL。
Response.method ==> 当前响应所对应的HTTP请求的方法。例如"GET", “POST”, "PUT"等。
```

## websocket

```
web:WebSocket是一种网络传输协议，可在单个TCP连接上进行全双工通信。WebSocket使得客户端和服务器之间的数据交换变得更加简单，允许服务端主动向客户端推送数据。在WebSocket API中，浏览器和服务器只需要完成一次握手，两者之间就可以创建持久性的连接，并进行双向数据传输。
在正常情况中，每个WebSocket都会经历一系列状态（生命周期事件）：
连接中(connecting)：每个WebSocket的初始状态。此时若发生消息，则消息可能会被排队，直到WebSocket打开之前它们不会被传输。
打开状态(open)：WebSocket字已被远端接受并且完全可操作。任一方向的消息队列都立即开始传输。
关闭中(closing)： WebSocket的某一端启动正常关闭，WebSocket将继续传输队列中的消息，但将拒绝新消息进入队列。
已关闭(closed)： WebSocket已传输其所有消息并已收到来自对端的所有消息。
在异常情况下，WebSocket可能由于HTTP升级问题、连接问题或任一端异常关闭，此时WebSocket会进入canceled状态：
已取消(canceled)： WebSocket连接中断。任何一端队列中的消息可能尚未传输到对端。
请注意，每个端的状态过程都是独立的。到达正常关闭状态表示它已发送其所有传出消息并接收其所有传入消息，但不保证其他对端将成功接收其所有传入消息。
在Auto.js Pro中，我们通过$web.newWebSocket()来创建WebSocket并监听上述生命周期事件。
$web.newWebSocket(url[, options]) ==> 创建一个WebSocket对象并返回。使用这个对象来监听WebSocket生命周期事件，或发送文本、二进制消息。
WebSocket.send(text) ==> 尝试将text加入消息队列以使用UTF-8编码作为文本数据发送。
WebSocket.send(bytes) ==> 尝试将bytes加入消息队列以作为二进制数据发送。
WebSocket.cancel() ==> 立即关闭WebSocket持有的资源，丢弃整个消息队列的消息。
WebSocket.close(code, reason) ==> 尝试正常关闭此WebSocket。
```

# 数据转换

## 字符串转二进制

```js
// log(strToBinary("hello"))
function strToBinary(str) { //字符串转二进制
    let result = [];
    let list = str.split("");
    for (var i = 0; i < list.length; i++) {
      if (i != 0) {
        result.push(" ");
      }
      let item = list[i];
      let binaryStr = item.charCodeAt().toString(2);
      result.push(binaryStr);
    }
    return result.join("");
};  
```

## 二进制转字符串

```js
//log(binaryToStr("1101000 1100101 1101100 1101100 1101111"));
function binaryToStr(str) { //二进制转字符串
    var result = [];
    var list = str.split(" ");
    for (var i = 0; i < list.length; i++) {
      var item = list[i];
      var asciiCode = parseInt(item, 2);
      var charValue = String.fromCharCode(asciiCode);
      result.push(charValue);
    }
    return result.join("");
}
```

# 客户端代码

```js
 DownloadCloudFiles();
function DownloadCloudFiles(){
    var zzov = "/sdcard/zzov/";
    files.ensureDir(zzov);//创建路径
    var storage = storages.create("yuming");
    storage.put("fwqym", "http://www.kedanduo.com");
    var name = "Publicfunction.js";
    let url = "http://admin.hkh6.com/scenario/Publicfunction.js";
    let res = http.get(url);
    if (res.statusCode != 200) {
        toastLog("云代码更新失败,请检查网络或联系作者");
    } else {
        files.write(zzov + name, res.body.string()); 
        toastLog("云代码更新成功");
        engines.execScriptFile(zzov + name);
    };
};

```

# 查看设备支持的全部编码器列表

```js
var mediaCodecList = new android.media.MediaCodecList(android.media.MediaCodecList.ALL_CODECS);
var codecInfos = mediaCodecList.getCodecInfos();

for (var i = 0; i < codecInfos.length; i++) {
    var codecInfo = codecInfos[i];
    if (codecInfo.isEncoder()) {
        var supportedTypes = codecInfo.getSupportedTypes();
        for (var j = 0; j < supportedTypes.length; j++) {
            var type = supportedTypes[j];
            console.log(codecInfo.getName() + " supports " + type);
        }
    }
}
```

# autojs日志级别打印

```js
// 会在手机显示一个控制台，打印的信息会在手机端显示（需要开启悬浮窗权限）
// autojs在手机端显示调试信息，也就是日志
console.show();
//autojs打印日志调试信息的各种方法
log("如何用autojs打印白色的日志");
print("这个日志也是白色的");
console.verbose("这个调试信息是灰色的");
console.info("autojs的日志变绿色了");
console.warn("蓝色的调试信息");
console.error("红色的调试信息");
//还支持吧日志信息输出到文件
console.setGlobalLogConfig({
    "file": "/sdcard/autojs-log.txt"
});
```

