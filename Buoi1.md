# Mở đầu về JAVA
## I. Ngôn ngữ Java là gì ?
*`Java là ngôn ngữ lập trình bậc cao, hướng đối tượng và giúp bảo mật mạnh mẽ.`*
- Java được phát triển bởi SunMicrosystems, do James Gosling khởi xướng và ra mắt năm 1995.
- Có thể ***chạy trên mọi nền tảng***, cung cấp cho người dùng cơ sở để có thể **"viết một lần, chạy mọi nơi"**.
## II. Lí do ra đời của Java
- Công ty Sun Microsystems giao cho Gosling xây dựng phần mềm cho các thiết bị dân dụng. Ban đầu Gosling và team định lựa chọn C++ nhưng mà C++ có vấn đề là khi chuyển sang chạy trên một hệ thống có bộ vi xử lý khác thì đòi hỏi phải biên dịch lại.
- Gosling quyết định xây dựng 1 ngôn ngữ mới dựa trên C++ đặt tên là **Oak**. Năm 1995, Oak đổi tên thành Java.
## III. Cách Java hoạt động, điều gì xảy ra khi chạy code Java (.java)
Quy trình hoạt động của Java được chia làm 3 bước chính:
- **Viết mã nguồn**: Lập trình viên viết mã nguồn Java trong các tệp .java.
- **Biên dịch mã nguồn**: Mã nguồn Java được biên dịch bởi trình biên dịch Java (Java Compiler) thành bytecode (tệp .class). Bytecode này không phải là mã máy mà máy tính có thể hiểu ngay, nhưng nó là dạng trung gian có thể được hiểu bởi bất kỳ hệ điều hành nào có JVM.
- **Chạy chương trình**: Bytecode sau đó được JVM thực thi. JVM dịch bytecode này thành mã máy (machine code) để hệ điều hành và phần cứng cụ thể có thể hiểu và thực thi chương trình.
![alt text](javaHD.png)
## IV. Cấu trúc 1 chương trình Java
```java
public class ClassName{
    public static void main(String[] args){
    //Các câu lệnh xử lý
  }
}
```
![alt text](cautrucJava.jpg)
## V. Package là gì
Package trong java là một group (nhóm) các class, interface và các package khác. Trong java chúng ta sử dụng package để tổ chức cấu trúc dự án hợp lý. Thông thường các class, interface và các package khác chứa trong package cha sẽ có những đặc điểm chung và xử lý cho các tình huống cụ thể.

Java có 2 loại package chính:
+ Package tích hợp sẵn.
Ví dụ: import java.util.Scanner;
Trong đó: 
  - **java**: package cha.
  - **util**: package con của java.
  - **Scanner**: là một class chứa trong package util.
+ Package tự định nghĩa.
## VI. Syntax cơ bản bao gồm:

#### 1.Khai báo biến nguyên thủy
| Kiểu    | Mô tả                                     | Mặc định | Cỡ      | Ví dụ                                        |
| ------- | ----------------------------------------- | -------- | ------- | -------------------------------------------- |
| boolean | true hoặc false                           | false    | 1 bit   | true, false                                  |
| byte    | Số nguyên từ -128 .. 127                  | 0        | 8 bits  | 123                                          |
| char    | Ký tự Unicode                             | \u0000   | 16 bits | 'a', '\u0041', '\101', '\\', '\'', '\n', 'ß' |
| short   | Số nguyên giá trị từ -32768 .. 32767      | 0        | 16 bits | 1000                                         |
| int     | Số nguyên -2,147,483,648 .. 2,147,483,647 | 0        | 32 bits | -2, -1, 0, 1, 2                              |
| long    | Số nguyên dài                             | 0        | 64 bits | -2L, -1L, 0L, 1L, 2L                         |
| float   | Số thực                                   | 0.0      | 32 bits | 1.23e100f, -1.23e-100f, .3f, 3.14F           |
| double  | Số thực                                   | 0.0      | 64 bits | 1.23456e300d, -1.23456e-300d, 1e1d           |
#### 2. Làm quen với vòng lặp
+ for():
```java
  for(int i = 1; i <= 10; ++i){
    System.out.println(i);
  }
```
+ while():
```java
  while(điều kiện){
    //code
  }
```
+ do-while:
```java
  do{
    //code
  }while(điều kiện);
```
#### 3. Câu lệnh rẽ nhánh
+ if-else:
```java
  if(điều kiện){
    //code 1
  }
  else if(điều kiện){
    //code 2
  }
  else {
    //code 3
  }
```
+ switch-case:
```java
  switch(dữ liệu){
    case 1:
      //code
      break;
    case n:
      //code
      break;
    default:
      //code
  }
```
#### 4. Mảng trong Java
Để khai báo một mảng, ta có 3 cách khai báo:
+ datatype[] arr;
+ datatype []arr;
+ datatype arr[];
Ví dụ:
```java
String[] class = {"Name", "Birth", "ID"};
System.out.println(class[0]);
```
## VII. Tổng quan về Class và Object:
+ ***Class (Lớp)***: 
  * Trong Java, một lớp là một thực thể xác định hành vi mà một đối tượng có và sẽ có. Nói cách khác, một lớp chỉ là một bản thiết kế hoặc một tập hợp các hướng dẫn để xây dựng các đặc tính của một đối tượng cụ thể sau này. Cách tạo lớp trong Java như sau:
```java
  class <class_name> {
    field;
    method;
  }
```
  + Trong đó:
    * **class**: Từ khóa để tạo 1 class.
    * **<class_name>**: Tên class được viết liền, viết **HOA** chữ cái đầu tiên của từng từ (Quy tắc PascalCase).
    * **field**: Đối tượng.
    * **method**: Phương thức.

+ ***Object (Đối tượng)***: 
  * Một Object có thể chứa các thành phần như các phương thức (method) và thuộc tính (thuộc tính) để tạo ra các kiểu dữ liệu hữu ích. Đối tượng xác định hành vi của lớp. Khi bạn gửi tin nhắn đến một đối tượng, bạn bắt buộc phải gọi đối tượng hoặc thực hiện một trong các phương thức của nó. 
  
  * Từ quan điểm của lập trình hướng đối tượng, các đối tượng có thể là cấu trúc dữ liệu, biến hoặc hàm. Đối tượng là vị trí bộ nhớ được cấp phát. Các đối tượng được thiết kế dưới dạng các lớp phân cấp. Cách tạo đối tượng trong Java như sau:
    ```java
    <class_name> ReferenceVariable = new <class_name>();
    ```
  + Trong đó:
      * **<class_name>**: Kiểu dữ liệu của đối tượng.
      * **ReferenceVariable**: Tên tham chiếu của đối tượng.
      * **new**: Từ khóa dùng tạo đối tượng.
      * **<class_name>()**: class dùng để tạo bạn đối tượng.

* ***Hình ảnh mô tả Class và Object***
![alt text](classandobject.jpg)
#### 1. This
**Trong java, Từ khóa this có 6 cách sử dụng như sau:**

* a. Từ khóa this có thể được dùng để tham chiếu tới **biến instance** của lớp hiện tại. 
  * Ví dụ:
  ```java
    public class Student10 {
      int id;
      String name;
  
      Student10(int id, String name) {
          id = id;
          name = name;
      }
  
      void display() {
          System.out.println(id + " " + name);
      }
  
      public static void main(String args[]) {
          Student10 s1 = new Student10(111, "Viet");
          Student10 s2 = new Student10(222, "Nam");
          s1.display();
          s2.display();
      }
  } 
  ```
* b. this() có thể được dùng để gọi **Constructor** của lớp hiện tại.
  * Ví dụ:
  ```java
    public class Student14 {
      int id;
      String name;
      String city;
  
      Student14(int id, String name) {
          this.id = id;
          this.name = name;
      }
  
      Student14(int id, String name, String city) {
          this(id, name);// now no need to initialize id and name
          this.city = city;
      }
  
      void display() {
          System.out.println(id + " " + name + " " + city);
      }
  
      public static void main(String args[]) {
          Student14 e1 = new Student14(111, "Viet");
          Student14 e2 = new Student14(222, "Nam", "Ha Noi");
          e1.display();
          e2.display();
      }
    } 
  ```
  *Chú ý*:  Nếu biến cục bộ và biến toàn cục có tên khác nhau thì không cần dùng this.
* c. Từ khóa this có thể được dùng để gọi **phương thức** của lớp hiện tại.
  * Ví dụ:
  ```java
    public class Example3 {
      void m() {
          System.out.println("Gọi phương thức bằng từ khóa this");
      }
  
      void n() {
          this.m();
      }
  
      void p() {
          n();// trình biên dịch sẽ thêm this để gọi phương thức n() như this.n()
      }
  
      public static void main(String args[]) {
          Example3 o1 = new Example3();
          o1.p();
      }
  }
  ```
* d. Từ khóa this có thể được **truyền như một tham số trong phương thức**.
  * Ví dụ:
  ```java
    public class Example4 {
      void m(Example4 obj) {
          System.out.println("Hello Java");
      }
  
      void p() {
          m(this);
      }
  
      public static void main(String args[]) {
          Example4 o1 = new Example4();
          o1.p();
      }
    }
  ```
* e. Từ khóa this có thể được **truyền như một tham số trong phương Constructor**.
    * Ví dụ:
  ```java
    class B {  
      A4 obj;  
      B(A4 obj) {  
        this.obj=obj;  
      }  
      void display() {  
        System.out.println(obj.data);// sử dụng biến thành viên cửa lớp A4
      }  
    } 

    class A4 {  
      int data=10;

      A4(){  
        B b = new B(this);  
        b.display();  
      }  

      public static void main(String args[]) {  
        A4 a = new A4();  
      }  
    }  
  ```
* f. Từ khóa this có thể được dùng để **trả về instance** của lớp hiện tại.
    * Ví dụ:
  ```java
    class A {  
      A getA() {  
        return this;  
      }  

      void msg() {
        System.out.println("Hello Java");
      }  
    } 

    class Test1 {  
      public static void main(String args[]) {  
        new A().getA().msg();  
      }  
    } 
  ``` 
#### 2. Constructor
* Constructor trong java là một dạng đặc biệt của phương thức được sử dụng để khởi tạo các đối tượng.

* Java Constructor được gọi tại thời điểm tạo đối tượng. Nó khởi tạo các giá trị để cung cấp dữ liệu cho các đối tượng, đó là lý do tại sao nó được gọi là constructor.

* Có 2 quy tắc cơ bản cho việc tạo constructor:
  *  Tên constructor phải giống tên lớp chứa nó.
  * Constructor không có kiểu trả về tường minh.

* Các kiểu của java constructor
  Có 2 kiểu của constructor:
  * Constructor mặc định (không có tham số truyền vào):
    * Cú pháp: 
  ```java
    <class_name>() {
      // code
    } 
  ``` 
    * Ví dụ:
  ```java
  class Bike1 {  
    Bike1() {
      System.out.println("Bike is created");
    }  
        
    public static void main(String args[]) {  
      Bike1 b=new Bike1();  
    }  
  } 
  ```
    * Mục đích: Constructor mặc định cung cấp các giá trị mặc định như 0, null, (tùy thuộc vào kiểu dữ liệu) ... tới đối tượng được khởi tạo.
  * Constructor tham số:
    * Một constructor có tham số truyền vào được gọi là constructor tham số.
    * Constructor tham số được sử dụng để cung cấp các giá trị khác nhau cho các đối tượng khác nhau.
    * Ví dụ:
    ```java
    class Student4{  
        int id;  
        String name;  
        Student4(int i,String n) {  
            id = i;  
            name = n;  
        }  
        void display() {
            System.out.println(id+" "+name);
        }  
        public static void main(String args[]) {  
            Student4 s1 = new Student4(111,"Viet");  
            Student4 s2 = new Student4(222,"Tuts");  
            s1.display();  
            s2.display();  
      }  
    }
    ```  
#### 3. Access modifier
* Access modifier trong Java xác định quyền truy cập trên các biến, các phương thức của class này từ các class khác trong cùng package hoặc ở hai package khác nhau.

* Có bốn loại access modifier trong Java đó là: public, protected, default và private. Tổng quan mỗi loại access modifier có ý nghĩa như sau:

  * **public**: tất cả các class khác trong hay ngoài package và nội bộ class đều có thể truy cập đến các biến, các phương thức public của class này.
  * **protected**: chỉ những class ở cùng package hoặc những class extends từ class này và nội bộ class mới có thể truy cập đến các biến, phương thức public của class này.
  * **default**: chỉ những class ở cùng package với class này và nội bộ class thì mới có thể truy cập đến các biến, các phương thức public của class này.
  * **private**: chỉ những class nằm bên trong class này mới có quyền truy cập đến các biến, phương thức public của class này.
* ***Public access modifier***:
  * Đây là access modifier ít giới hạn quyền truy cập nhất, các public class hoặc interface có thể được truy cập từ tất cả các package, bao gồm nội bộ class hoặc inteface cho đến các class nằm trong các package khác nhau.
* ***Protected access modifier***:
  * Các biến, các phương thức được định nghĩa với protected access modifier chỉ có truy cập từ các class nằm trong cùng package và các class con extends từ class này.
* ***Default access modifier***:
  * Các biến, các phương thức được định nghĩa mà không sử dụng một access modifier nào thì nó sẽ có access modifier mặc định. Những biến, phương thức này chỉ có thể truy cập từ các class nằm trong cùng package.
* ***Private access modifier***:
  * Đây là access modifer giới hạn quyền truy cập nhiều nhất, với access modifier này các biến, các phương thức của chúng ta chỉ có thể truy cập ở bên trong class.
#### 4. Setter và Getter:
* Setter và Getter là 2 phương thức sử dụng để cập nhật hoặc lấy ra giá trị thuộc tính, đặc biệt dành cho các thuộc tính ở phạm vi private.

* Việc sử dụng Setter và Getter cần thiết trong việc kiểm soát những thuộc tính quan trọng mà ta thường được sử dụng và yêu cầu giá trị chính xác. Ví dụ thuộc tính age lưu tuổi con người, thực tế thì phạm vi tuổi là từ 0 đến 100, thì ta không thể cho chương trình lưu giá trị age âm hoặc quá 100 được.

* Cú pháp:
  * Setter:
  ```java
  public void set<tên thuộc tính> (<tham số giá trị mới>) {
        this. <tên thuộc tính> = <tham số giá trị mới>;
  }
  ```
  * Getter:
  ```java
  <kiểu dữ liệu thuộc tính> get<tên thuộc tính> () {
        return this. <tên thuộc tính>;
  }
  ```
* Chú ý:
  * Khi đã dùng setter và getter thì thuộc tính nên để private.
  * Cẩn thận với kiểu dữ liệu tham chiếu.
#### 6. Từ khóa static
* Từ khóa static trong Java được sử dụng chính để quản lý bộ nhớ. Chúng ta có thể áp dụng từ khóa static với các biến, các phương thức, các khối, các lớp lồng nhau(nested class). Từ khóa static thuộc về lớp chứ không thuộc về instance(thể hiện) của lớp.

* Trong java, Static có thể là:

  * *Biến static*: Khi bạn khai báo một biến là static, thì biến đó được gọi là biến tĩnh, hay biến static.
  * *Phương thức static*: Khi bạn khai báo một phương thức là static, thì phương thức đó gọi là phương thức static.
  * *Khối static*: Được sử dụng để khởi tạo thành viên dữ liệu static.