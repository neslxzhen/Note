# 記事本存檔預設值改為UTF-8、Unicode格式
###### tags: `windows` `regedit` `encoding`
## 參考
  - [[pixnet] 記事本存檔預設值改為utf-8、unicode格式](http://macrosshiking.pixnet.net/blog/post/197940064-記事本存檔預設值改為utf-8、unicode格式)

## 步驟
### Step 1
將空白記事本以UTF-8、Unicode儲存到路徑: `C:\Windows\ShellNew`

### Step 2
開啟登陸編輯器 (regedit)

### Step 3
找到`HKEY_CLASSES_ROOT\.txt\ShellNEW`

### Step 4
在右方新增字串，名稱: `FileName`

### Step 5
數值資料: `TXTUTF-8.txt` 或是 `TXTUnicode.txt`

### Fin.
在任何地方新增一個記事本，另存若編碼為 `UTF-8` 或是 `Unicode` 則成功。