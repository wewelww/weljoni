# 创建文件的三种方式
## 1. 根据路径创建File对象
- 方法：`new File(String pathname)`
```java
package src.IOStream;  

import java.io.File;  
import java.io.IOException;  

// 根据路径创建一个 File 对象  
public class newFile {  
    public static void main(String[] args) {  
        createFile();  
 }  
    public static void createFile(){  
        File file = new File("Serialable/src/IOStream/CreateForFile/new1.txt");  
 try{  
            file.createNewFile();  
 System.out.println("Create Successfully");  
 } catch (IOException e){  
            e.printStackTrace();  
 }  
    }  
}
```

定义当前类`newfile`的包名
`package src.IOStream;`
`src.IOStream` 表示当前类位于 `src` 目录下的 `IOStream` 包中。

导入java的输入输出类
`import java.io.File;`
`import java.io.IOException;`
- `java.io.File`：提供了创建、删除、读取文件等功能。
- `java.io.IOException`：处理输入输出时可能抛出的异常（比如文件无法创建、权限不足等）。

`public static void main`定义了一个方法，该方法是静态的，可以直接用类名调用。

![[Pasted image 20241205172818.png]]

## 2. 根据父目录File对象在子路径创建一个文件
- 方法 `new File(File parent, String child)`
```java
package src.IOStream;  
  
import java.io.File;  
import java.io.IOException;  
  
// 根据父目录File对象，在子路径创建一个文件  
public class newFile02 {  
    public static void main(String[] args) {  
        createFile();  
 }  
    public static void createFile(){  
        File parentFile = new File("Serialable/src/IOStream/CreateForFile");  
 File file = new File(parentFile, "new2.txt");  
 try{  
            file.createNewFile();  
 System.out.println("Create Successfully");  
 } catch (IOException e){  
            e.printStackTrace();  
 }  
    }  
}
```

![[Pasted image 20241205172838.png]]

## 3. 根据父目录路径，在子路径下生成文件
- 方法 `new File(String parent, String child)`
```java
package src.IOStream;  
  
import java.io.File;  
import java.io.IOException;  
  
// 根据父目录路径，在子路径下生成文件  
public class newFile03 {  
    public static void main(String[] args) {  
        createFile();  
 }  
    public static void createFile(){  
        String parentPath = "Serialable/src/IOStream/CreateForFile";  
 String fileName = "new3.txt";  
 File file = new File(parentPath, fileName);  
 try{  
            file.createNewFile();  
 System.out.println("Create Successfully");  
 } catch (IOException e){  
            e.printStackTrace();  
 }  
    }  
}
```

![[Pasted image 20241205172900.png]]

# 获取文件信息
先在new1.txt中，写入一段话。
![[Pasted image 20241205173655.png]]

通过file类的方法获取一些基本信息：
```java
package src.IOStream;  
  
import java.io.File;  
  
public class GetFileInfo {  
    public static void main(String[] args) {  
        getFileContents();  
 }  
  
    public static void getFileContents(){  
        File file = new File("Serialable/src/IOStream/CreateForFile/new1.txt");  
 System.out.println("文件名称为：" + file.getName());  
 System.out.println("文件的绝对路径为：" + file.getAbsolutePath());  
 System.out.println("文件的父级目录为：" + file.getParent());  
 System.out.println("文件的大小(字节)为：" + file.length());  
 System.out.println("这是不是一个文件：" + file.isFile());  
 System.out.println("这是不是一个目录：" + file.isDirectory());  
 }  
}
```

![[Pasted image 20241205173857.png]]

# 目录与文件操作
## 1. 文件删除
- 方法：`file.delete(文件)`
```java
package src.IOStream;  
  
import java.io.File;  
import java.lang.reflect.Field;  
  
// 文件删除  
public class FileDelete {  
    public static void main(String[] args) {  
        deleteFile();  
 }  
    public static void deleteFile(){  
        File file = new File("Serialable/src/IOStream/CreateForFile/new1.txt");  
 System.out.println(file.delete() ? "Delete Successfully":"Delete failed");  
 }  
}
```

![[Pasted image 20241205203530.png]]

## 2. 目录删除
- 方法 `file.delete(目录)`注意只有空的目录才可以删除，不然会显示删除失败。
```java
package src.IOStream;  
  
import java.io.File;  
  
//删除目录  
public class DirectoryDelete {  
    public static void main(String[] args) {  
        deleteDirectory();  
 }  
    public static void deleteDirectory(){  
        File file = new File("Serialable/src/IOStream/CreateForDelete");  
 System.out.println(file.delete()? "Delete Successfully":"Delete failed");  
 }  
}
```

![[Pasted image 20241205213334.png]]

## 3. 创建单级目录
- 方法 `file.mkdir()`
```java
package src.IOStream;  
  
import java.io.File;  
  
// 创建单级目录  
public class CreateSingleDirectory {  
    public static void main(String[] args) {  
        createSingleDir();  
 }  
    public static void createSingleDir(){  
        File file = new File("Serialable/src/IOStream/CreateForDirectory");  
 System.out.println(file.mkdir() ? "Create Successfully":"Create failed");  
 }  
}
```

![[Pasted image 20241206125636.png]]

## 4. 创建多级目录
方法 `file.mkdirs()`
```java
package src.IOStream;  
  
import java.io.File;  
  
// 创建多级目录  
public class CreateMultiDirectory {  
    public static void main(String[] args) {  
        createMultiDir();  
 }  
  
    public static void createMultiDir(){  
        File file = new File("Serialable/src/IOStream/CreateMultiDirectory/test");  
 System.out.println(file.mkdirs() ? "Create Successfully":"Create failed");  
  
 }  
}
```

![[Pasted image 20241206141756.png]]

# IO流分类
按照操作数据单位不同分为：字节流和字符流
- 字节流（8bit，适用于二进制文件）
- 字符流（按字符，因编码不同而异，适用于文本文件）

按照数据流流向不同分为：输入流和输出流
按照流的角色不同分为：节点流，处理流/包装流

|抽象基类|字节流|字符流|
|---|---|---|
|输入流|InputStream|Reader|
|输出流|OutputStream|Writer|

# 文件流的一些操作
## 1. Runtime命令执行操作的Payload
```java
package src.CommandExec;  
  
import java.io.ByteArrayOutputStream; //ByteArrayOutputStream：用于将字节流输出到内存中的字节数组，并能够转换为字符串。
import java.io.InputStream;  //InputStream：用于读取命令的输出流。
  
// 使用 Runtime 类进行命令执行  
public class RuntimeExec {  
    public static void main(String[] args) throws Exception {  
        InputStream inputStream = Runtime.getRuntime().exec("whoami").getInputStream();  
 byte[] cache = new byte[1024];  //缓存数据
 ByteArrayOutputStream byteArrayOutputStream = new ByteArrayOutputStream();  //创建一个ByteArrayOutputStream对象，用于将读取到的字节数据存储到内存中的字节数组。
 int readLen = 0;  
 while ((readLen = inputStream.read(cache))!=-1){  
            byteArrayOutputStream.write(cache, 0, readLen);  
 }  
        System.out.println(byteArrayOutputStream);  
 }  
}
```

## 2. FileInputStream
### read() 方法
点击read方法，跳进去读一下。
![[Pasted image 20241206154026.png]]

```java
public int read(byte[] b) throws IOException {  
    return read(b, 0, b.length);  
}  
  
/**  
 * Reads up to {@code len} bytes of data from the input stream into  
 * an array of bytes.  An attempt is made to read as many as * {@code len} bytes, but a smaller number may be read.  
 * The number of bytes actually read is returned as an integer. * * <p> This method blocks until input data is available, end of file is  
 * detected, or an exception is thrown. * * <p> If {@code len} is zero, then no bytes are read and  
 * {@code 0} is returned; otherwise, there is an attempt to read at  
 * least one byte. If no byte is available because the stream is at end of * file, the value {@code -1} is returned; otherwise, at least one  
 * byte is read and stored into {@code b}.  
 * * <p> The first byte read is stored into element {@code b[off]}, the  
 * next one into {@code b[off+1]}, and so on. The number of bytes read  
 * is, at most, equal to {@code len}. Let <i>k</i> be the number of  
 * bytes actually read; these bytes will be stored in elements * {@code b[off]} through {@code b[off+}<i>k</i>{@code -1]},  
 * leaving elements {@code b[off+}<i>k</i>{@code ]} through  
 * {@code b[off+len-1]} unaffected.  
 * * <p> In every case, elements {@code b[0]} through  
 * {@code b[off-1]} and elements {@code b[off+len]} through  
 * {@code b[b.length-1]} are unaffected.  
 * * @implSpec  
 * The {@code read(b, off, len)} method  
 * for class {@code InputStream} simply calls the method  
 * {@code read()} repeatedly. If the first such call results in an  
 * {@code IOException}, that exception is returned from the call to  
 * the {@code read(b,} {@code off,} {@code len)} method.  If  
 * any subsequent call to {@code read()} results in a  
 * {@code IOException}, the exception is caught and treated as if it  
 * were end of file; the bytes read up to that point are stored into * {@code b} and the number of bytes read before the exception  
 * occurred is returned. The default implementation of this method blocks * until the requested amount of input data {@code len} has been read,  
 * end of file is detected, or an exception is thrown. Subclasses are * encouraged to provide a more efficient implementation of this method. * * @param      b     the buffer into which the data is read.  
 * @param      off   the start offset in array {@code b}  
 *                   at which the data is written. * @param      len   the maximum number of bytes to read.  
 * @return     the total number of bytes read into the buffer, or  
 *             {@code -1} if there is no more data because the end of  
 *             the stream has been reached. * @throws     IOException If the first byte cannot be read for any reason  
 *             other than end of file, or if the input stream has been closed, *             or if some other I/O error occurs. * @throws     NullPointerException If {@code b} is {@code null}.  
 * @throws     IndexOutOfBoundsException If {@code off} is negative,  
 *             {@code len} is negative, or {@code len} is greater than  
 *             {@code b.length - off}  
 * @see        java.io.InputStream#read()  
 */public int read(byte[] b, int off, int len) throws IOException {  
    Objects.checkFromIndexSize(off, len, b.length);  
    if (len == 0) {  
        return 0;  
    }  
  
    int c = read();  
    if (c == -1) {  
        return -1;  
    }  
    b[off] = (byte)c;  
  
    int i = 1;  
    try {  
        for (; i < len ; i++) {  
            c = read();  
            if (c == -1) {  
                break;  
            }  
            b[off + i] = (byte)c;  
        }  
    } catch (IOException ee) {  
    }  
    return i;  
}
```

参数：
`b`：用于存储读取数据的字节数组。
`off`：数据存储在数组b中的起始偏移量。
`len`：要读取的最大字节数。

返回值：
返回实际读取的字节数（读取成功）
如果到达文件末尾，返回-1。

现在我们用`FileInputStream.read()`来读取文件。
```java
package src.IOStream;  
  
import java.io.FileInputStream;  
import java.io.IOException;  
  
// 使用 FileInputStream.read 读取文件  
public class FileInputRead {  
    public static void main(String[] args) {  
        readFile();  
 }  
    public static void readFile(){  
        String filePath = "Serialable/src/IOStream/CreateForFile/new1.txt";  
 FileInputStream fileInputStream = null;  
 int readData = 0;  
 try{  
            fileInputStream = new FileInputStream(filePath);  
 while((readData = fileInputStream.read())!=-1){  
                System.out.print((char)readData);  
 }  
        } catch (IOException e){  
            e.printStackTrace();  
 } finally {  
            try{  
                fileInputStream.close();  
 } catch (IOException e){  
                e.printStackTrace();  
 }  
        }  
    }  
}
```

![[Pasted image 20241206165118.png]]

### read(byte[] d) 方法
允许在方法中添加一个字节数组。  
这种方式很有意思，当我们设置缓冲区的值为 8 时，若文件中的字符长度超过了 8，则会换行输出。
```java
package src.IOStream;  
  
import java.io.FileInputStream;  
import java.io.IOException;  
  
// read(byte[] d) 方法，允许在方法中添加一个字节数组  
public class FileInputRead02 {  
    public static void main(String[] args) {  
        readFile();  
 }  
    public static void readFile(){  
        String filePath = "Serialable/src/IOStream/CreateForFile/new1.txt";  
 FileInputStream fileInputStream = null;  
 byte[] cache = new byte[8]; // 设置缓冲区，缓冲区大小为 8 字节  
 int readLen = 0;  
 try {  
            fileInputStream = new FileInputStream(filePath);  
 while((readLen = fileInputStream.read(cache)) != -1){  
                System.out.println(new String(cache, 0, readLen));  
 }  
        } catch (IOException e){  
                e.printStackTrace();  
 } finally {  
            try {  
                fileInputStream.close();  
 } catch (IOException e){  
                e.printStackTrace();  
 }  
        }  
    }  
}
```

![[Pasted image 20241206171840.png]]

## 3. FileOutputStream
### write(byte[] b) 方法
```java
write(byte[] b)
public void write(byte[] b)
           throws IOException
将 b.length 个字节从指定 byte 数组写入此文件输出流中。
覆盖：
类 OutputStream 中的 write
参数：
b - 数据。
抛出：
IOException - 如果发生 I/O 错误。
```

```java
package src.IOStream;  
  
import java.io.FileNotFoundException;  
import java.io.FileOutputStream;  
import java.io.IOException;  
  
// write(byte[] b) 方法  
public class FileOutputWrite01 {  
    public static void main(String[] args) {  
        writeFile();  
 }  
  
    public static void writeFile() {  
        String filePath = "Serialable/src/IOStream/CreateForFile/new1.txt";  
 FileOutputStream fileOutputStream = null;  
 try { // 注意fileOutputStream的作用域，因为fileOutputStream需要在finally分支中被异常捕获  
 // 所以这里的 try 先不闭合  
 fileOutputStream = new FileOutputStream(filePath);  
 String content = "hellohello";  
 try {  
                //write(byte[] b) 将 b.length 个字节从指定 byte 数组写入此文件输出流中  
 //String类型的字符串可以使用getBytes()方法将字符串转换为byte数组  
 fileOutputStream.write(content.getBytes());  
 } catch (IOException e) {  
                e.printStackTrace();  
 }  
        }catch (FileNotFoundException e){  
            e.printStackTrace();  
 }  
        finally {  
            try {  
                fileOutputStream.close();  
 } catch (IOException e){  
                e.printStackTrace();  
 }  
        }  
    }  
}
```

![[Pasted image 20241206173029.png]]

### write(byte[] b, int off, int len) 方法
- 将指定 byte 数组中从偏移量 off 开始的 len 个字节写入此文件输出流。
```java
package src.IOStream;  
  
import java.io.FileNotFoundException;  
import java.io.FileOutputStream;  
import java.io.IOException;  
import java.nio.charset.StandardCharsets;  
  
// write(byte[] b) 方法  
public class FileOutputWrite02 {  
    public static void main(String[] args) {  
        writeFile();  
 }  
  
    public static void writeFile() {  
        String filePath = "Serialable/src/IOStream/CreateForFile/new1.txt";  
 FileOutputStream fileOutputStream = null;  
 try { // 注意fileOutputStream的作用域，因为fileOutputStream需要在finally分支中被异常捕获  
 // 所以这里的 try 先不闭合  
 fileOutputStream = new FileOutputStream(filePath);  
 String content = "hihi";  
 try {  
                //write(byte[] b) 将 b.length 个字节从指定 byte 数组写入此文件输出流中  
 //String类型的字符串可以使用getBytes()方法将字符串转换为byte数组  
 fileOutputStream.write(content.getBytes(StandardCharsets.UTF_8), 0, 4);  
 } catch (IOException e) {  
                e.printStackTrace();  
 }  
        }catch (FileNotFoundException e){  
            e.printStackTrace();  
 }  
        finally {  
            try {  
                fileOutputStream.close();  
 } catch (IOException e){  
                e.printStackTrace();  
 }  
        }  
    }  
}
```

![[Pasted image 20241206173352.png]]

### 追加写入
如果想要写入的数据不被覆盖，可以设置 `FileOutputStream` 的构造方法 `append` 参数设置为 `true`。

## 4. 文件拷贝 ———— input outp 结合
```java
package src.IOStream;  
  
import java.io.FileInputStream;  
import java.io.FileOutputStream;  
import java.io.IOException;  
  
// 文件拷贝操作  
public class FileCopy {  
    public static void main(String[] args) {  
            copyFile();  
 }  
    public static void copyFile(){  
        String srcFilename = "Serialable/src/IOStream/CreateForFile/new1.txt";  
 String desFilename = "Serialable/src/IOStream/CreateForFile/new2.txt";  
 FileInputStream fileInputStream = null;  
 FileOutputStream fileOutputStream = null;  
 try {  
            fileInputStream = new FileInputStream(srcFilename);  
 fileOutputStream = new FileOutputStream(desFilename);  
 byte[] cache = new byte[1024];  
 int readLen = 0;  
 while((readLen = fileInputStream.read(cache)) != -1){  
                fileOutputStream.write(cache, 0, readLen);  
 }  
    } catch (IOException e){  
            e.printStackTrace();  
 } finally {  
            try {  
                fileInputStream.close();  
 fileOutputStream.close();  
 } catch (IOException e){  
                e.printStackTrace();  
 }  
        }  
        }  
}
```

![[Pasted image 20241206210527.png]]

## 5. FileReader
```java
package src.IOStream;  
  
import java.io.FileReader;  
import java.io.IOException;  
  
// 读取文件的字符流  
public class FileReaderPrint {  
    public static void main(String[] args) {  
        readFile();  
 }  
    public static void readFile(){  
        String filePath = "Serialable/src/IOStream/CreateForFile/new1.txt";  
 FileReader fileReader = null;  
 try {  
            fileReader = new FileReader(filePath);  
 int readLen = 0;  
 char[] cache = new char[8];  
 while ((readLen = fileReader.read(cache))!=-1){  
                System.out.println(new String(cache, 0, readLen));  
 }  
        } catch (IOException e){  
            e.printStackTrace();  
 } finally {  
            try {  
                fileReader.close();  
 } catch (IOException e){  
                e.printStackTrace();  
 }  
        }  
    }  
}
```

![[Pasted image 20241206213551.png]]



























