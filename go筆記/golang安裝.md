# golang安裝

 目標Ubuntu18.04
 
透過 wget 下載

    wget https://dl.google.com/go/go1.14.6.linux-amd64.tar.gz 

解壓縮gz

    sudo tar -xvf go1.11.5.linux-amd64.tar.gz
    
把 binary 檔放到 /usr/local:

    sudo mv go /usr/local
    
然後設定 Golang 的環境變數, 一般需要設定 GOROOT, GOPATH 及 PATH, 開啟 .profile 檔:

    sudo nano  ~/.profile


加入以下內容:
GOROOT: Golang 安裝的目錄.
GOPATH: 工作的目錄, 儲存專案的目錄是 ~/go

    export GOROOT=/usr/local/go
    export GOPATH=$HOME/go
    export PATH=$GOPATH/bin:$GOROOT/bin:$PATH
    
儲存 .profile 後, 執行以下指令讓設定生效:

    source ~/.profile


建立第一支 Go 語言的 “Hello World!” 程式, 用文字編譯器建立 hello.go:

    sudo nano hello.go
    
加入以下程式碼:

    package main
    import "fmt"

    func main() {
         fmt.Println("Hello, World!\n")
    }  
    
    
接著就執行了, Go 語言不用編譯也可以先執行, 輸入以下指令:

    go run hello.go
    
要將程式碼編譯成二進制檔案, 用 build 選項:

    go build hello.go    
    
目錄下會產生 hello 檔案, 可以直接執行:

    ./hello
