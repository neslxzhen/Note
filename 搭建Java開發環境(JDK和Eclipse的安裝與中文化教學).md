# 搭建Java開發環境（JDK和Eclipse的安裝與中文化教學）
###### tags:`IDE` `Eclipse` `Java` `JDK`
 參考至:
  - http://www.weixueyuan.net/view/5945.html

要進行Java開發，首先要安裝JDK（Java Development Kit，Java開發工具箱）。

JDK 是一系列工具的集合，這些工具是編譯Java源碼、運行Java程式所必需的，例如JVM、基礎類庫、編譯器、打包工具等。不論是什麼樣的 Java 應用伺服器，都是內置了某個版本的 JDK，因此掌握 JDK 是學好 Java 的第一步。

JDK所提供的部分工具：

*   java編譯器：javac.exe

*   java解譯器：java.exe

*   java文檔生成器：javadoc.exe

*   java調試器：jdb.exe

前面所說的Java版本，實際上是指JDK的版本。

最主流的 JDK 是 Sun 公司發佈的 JDK，除了 Sun 之外，還有很多公司和組織都開發了自己的 JDK，例如 IBM 公司開發的 JDK、BEA 公司的 Jrocket，還有 GNU 組織開發的 JDK等等。IBM 的 JDK 包含的 JVM（Java Virtual Machine）運行效率要比 Sun JDK 包含的 JVM高出許多，而專門運行在 x86 平臺的 Jrocket，在服務端運行效率也要比 Sun JDK 好很多，但不管怎麼說，還是需要先把 Sun JDK 掌握好。

## JDK 的下載

JDK有不同的版本（J2SE、J2EE、J2ME），初學Java，一般都選擇J2SE。J2SE的下載地址為：http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html

打開網址，會看到如下所示的頁面：

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/1.png)

 > 圖1  J2SE(Java SE)下載頁面

下載JDK需要接受相應條款，預設是不能下載的。

選擇相應的作業系統，點擊下載連結即可下載。

## JDK的安裝

按兩下下載好的安裝包進行安裝，點擊“下一步”，出現如下圖所示的介面：

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/2.png)

 > 圖2  改變安裝目錄

這裡可以根據你的習慣改變JDK的安裝目錄，不過你要記住，後面會用到這個安裝目錄。

可以看到，JDK包含了Java開發工具（編譯器、打包工具等）、原始程式碼（基礎類庫）和公共JRE，這三項都是默認安裝的，是Java開發所必須的，缺一不可。

點擊“下一步”，等待安裝。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/3.png)

 > 圖3  正在安裝

JDK安裝完成後，會提示你是否安裝JRE，如下圖所示：

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/4.png)

 > 圖4  是否安裝JRE

JDK中已經包含了JRE，無需再次安裝，點擊“取消”即可。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/5.png)

 > 圖5  確認取消



![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/6.png)

 > 圖6  完成安裝

點擊“關閉”，完成安裝。

## 環境變數的設置

如果你不瞭解環境變數的概念，請猛擊這裡：[什麼是環境變數](http://www.weixueyuan.net/view/6310.html)

進入環境變數配置視窗，在“使用者變數”中，設置3項屬性，JAVA_HOME、PATH、CLASSPATH（大小寫無所謂），若已存在則點擊“編輯”，不存在則點擊“新建”：

· JAVA_HOME：設為JDK的安裝路徑(如D:\Program Files\jdk1.7.0_71)，此路徑下包括lib，bin，jre等資料夾（此變數最好設置，因為以後運行tomcat，eclipse等都需要依靠此變數）。

· Path：使得系統可以在任何路徑下識別java命令，設為：%JAVA_HOME%\bin。%JAVA_HOME%就是引用前面指定的JAVA_HOME變數。

· CLASSPATH：Java運行環境載入類的路徑，只有類在classpath中，才能被識別和載入，設為 .;%JAVA_HOME%\lib（注意前面的點號(.)，點號表示當前路徑）。

打開一個CMD視窗，輸入“java -version”或者“javac”命令，看到很多說明資訊，證明已經安裝並配置成功了。

## Eclipse的安裝

有了JDK，你可以編譯Java源碼，運行Java程式，但是還沒有代碼編輯器，沒有版本管理工具，也不能方便的管理工程檔，不能與團隊協作。安裝Eclipse，你才能完成這些工作。

Eclipse是一款Java整合式開發環境(IDE)。Java IDE有很多，有免費的，有收費的，有英文的，中文的，有多國語言的，Eclipse 是最常用的一款，IT公司大部分員工都使用Eclipse。

Eclipse 開源免費，使用人數最多，提供了豐富的外掛程式和友好的編輯介面，資源佔用比較低，速度比較快，本身就是用Java開發的。

注意：一定要設置環境變數，Eclipse 的運行依賴於這些環境變數。

Eclipse的下載地址為：http://www.eclipse.org/downloads/

打開連結，看到下面的頁面：

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/7.png)

 > 圖7  Eclipse 下載頁面

選擇紅色方框框起來的版本，下載即可。

Eclipse 是免安裝的，你可以將下載的壓縮檔解壓到任意目錄，以後也可以隨意更換目錄。第一次啟動Eclipse，會要求你設置預設的工程目錄，你可以只設置一次，也可以每次啟動都設置。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/8.png)

 > 圖8  設置工程目錄

點擊“OK”，Eclipse 就成功啟動，彈出歡迎介面。

## 安裝簡體中文語言包

Eclipse 默認是英文的，如果你的英文能力比較弱，可以安裝簡體中文語言包。不過我建議你使用英文版，作為程式師，你絕對有必要提高你的英文水準，很多技術文檔都是英文的，只要持之以恆，很快就能提高你的英文閱讀能力。

語言包的下載位址為：http://www.eclipse.org/babel/downloads.php

首先查看你當前安裝的Eclipse的版本。在Eclipse功能表列中選擇“Help --> About Eclipse”，彈出一個對話方塊：

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/9.png)

 > 圖9  查看Eclipse版本

打開連結，向下滾動滑鼠，下載對應版本的語言包：

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/10.png)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/11.png)

 > 圖10  對應版本的語言包

進入下載頁面，找到簡體中文語言包：

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/12.png)

 > 圖11  中文語言包

這裡包含了Eclipse軟體本身及其模組和外掛程式的語言包，你可以一次全部下載，也可以需要的時候再來下載，紅色方框框起來的是Eclipse軟體本身的中文包，我們需要下載它。

將下載到的檔解壓，得到一個名為eclipse的資料夾，它裡面包含兩個資料夾：features和plugins，複製features和plugins到你的eclipse安裝目錄，覆蓋原程式檔即可。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/搭建Java開發環境(JDK和Eclipse的安裝與中文化教學)/13.png)

 > 圖 12  覆蓋原來的文件

重啟Eclipse，漢化完成，你可以享受中文版的Eclipse了。

  
