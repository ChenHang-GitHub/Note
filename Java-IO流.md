# IO流   输入输出流

### IO理解分类 - 从传输方式上

- 字节流
- 字符流 

`字节`是个计算机看的，`字符`才是给人看的

### ![1649509245983](E:\TyporaNotes\Note\assets\1649509245983.png)

![1649509271457](E:\TyporaNotes\Note\assets\1649509271457.png)

### 字节流和字符流的区别

- 字节流读取单个字节，字符流读取单个字符(一个字符根据编码的不同，对应的字节也不同，如 UTF-8 编码是 3 个字节，中文编码是 2 个字节。)
- 字节流用来处理二进制文件(图片、MP3、视频文件)，字符流用来处理文本文件(可以看做是特殊的二进制文件，使用了某种编码，人可以阅读)。



###    IO理解分类 - 从数据操作上

- ### 文件(file)

- FileInputStream、FileOutputStream、FileReader、FileWriter

- ### [¶](#数组) 数组([])

- - 字节数组(byte[]): ByteArrayInputStream、ByteArrayOutputStream
  - 字符数组(char[]): CharArrayReader、CharArrayWriter

- ### [¶](#管道操作) 管道操作

- PipedInputStream、PipedOutputStream、PipedReader、PipedWriter

- ### [¶](#基本数据类型) 基本数据类型

- DataInputStream、DataOutputStream

- ### [¶](#缓冲操作) 缓冲操作

- BufferedInputStream、BufferedOutputStream、BufferedReader、BufferedWriter

- ### [¶](#打印) 打印

- PrintStream、PrintWriter

- ### [¶](#对象序列化反序列化) 对象序列化反序列化

- ObjectInputStream、ObjectOutputStream

- ### [¶](#转换) 转换

- InputStreamReader、OutputStreamWriter

### IO 装饰者模式

以 InputStream 为例，

- InputStream 是抽象组件；
- FileInputStream 是 InputStream 的子类，属于具体组件，提供了字节流的输入操作；
- FilterInputStream 属于抽象装饰者，装饰者用于装饰组件，为组件提供额外的功能。例如 BufferedInputStream 为 FileInputStream 提供缓存的功能。

![1649510003394](E:\TyporaNotes\Note\assets\1649510003394.png)

