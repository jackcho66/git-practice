介紹Git的操作
===

安裝完Git後，可開啟vscode檢查是否正確安裝
---

1.打開vscode左上角的Terminal-New Terminal
![alt text](image.png)

2.在底下視窗輸入`git --version`，如果有跑出版本號就代表已成功安裝
![alt text](image-2.png)

使用Git前必須先設定姓名和電子郵件，因為Git在記錄版本變更時也會記錄作者資訊
---

1.姓名設定方式為輸入`git config --global user.name "自己的姓名"`

2.電子郵件設定方式為輸入`git config --global user.email "自己的電子郵件"`

把目前資料夾轉成具有版本功能的儲存庫
---

輸入`git init` : 這個指令會在當前目錄建立一個隱藏.git子資料夾，用來儲存檔案變更歷史。不小心刪除的話==所有歷史和備分紀錄都會消失==

![alt text](image-3.png)
![alt text](image-4.png)

清空指令
---

終端機指令太多可以輸入`clear`來清空內容
![alt text](image-5.png)

檢查當前目錄中的檔名和狀態
---

輸入`git status`
![alt text](image-7.png)
紅字為未追蹤的檔案

由未追蹤變更為已追蹤
---

輸入`git add 檔案名稱`，送出後會發現左邊檔案列表所選的檔案會出現A代表已成功新增
![alt text](image-8.png)
![alt text](image-9.png)

可用`git status`再檢查一次，會用綠色來標示已追蹤的檔案
![alt text](image-10.png)

紀錄版本變更
---

若有做任何修改，左方檔案列表會出現M，提醒你尚未記錄。
![alt text](image-12.png)

這時先輸入`git add 檔案名稱`將欲紀錄的檔案加入追蹤
再輸入`git commit -m "內容"`，內容可隨意填寫
![alt text](image-13.png)

這時左方檔案列表的M就消失了代表已成功紀錄
![alt text](image-11.png)

檢視歷史紀錄
---

輸入`git log`，這個指令會顯示先前提交的修改紀錄(提交者、時間、說明文字)
，==按下q即可離開檢視==
![alt text](image-14.png)

另一個指令`git log --oneline`，這個指令是git log指令的簡化版，適合快速瀏覽過去紀錄
![alt text](image-15.png)
