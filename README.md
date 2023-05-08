# sftp_server
今天因為需要用到sftp協定來傳輸資料，擔心傳過來的資料很奇怪，不敢直接到server，又不想要再開一台VM，所以用Docker架設了sftp的server。
首先把image拉下來

'''
docker pull atmoz/sftp
'''

接著介紹參數
1.volume前面接的是接出來的本地資料夾，後面是container裡面的路徑，這樣的話可以在本地查看傳入container的資料。一定要用絕對路徑，不然會一直出現permission denied。
2.port設定轉送。
3.最後一行設定的是登入者與密碼，正確格式是 user:pass:UID:GID:dir
    
    
參考資料 : https://ithelp.ithome.com.tw/articles/10249127
