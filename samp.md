```go
package main

  import (
          "fmt"
          "time"
          "math/rand"
  )


  func main() {

       	start := time.Now()
        Matrix()
     
        elapsed := time.Since(start)

        fmt.Println("Elapsed time : ",elapsed)
  }


  func Matrix(){

        // Инициализация массивов
        row1 := []int{}
        row2 := []int{}
        row3 := []int{}
        

        // Stream:=4                      // количество потоков
        Matrix:=1000000                    // количество элементов
        rnd:=2000                      // парамтер для генерации случайных чисел в матрице

        // Заполнение масивов  
        // случайными числами от 0 до 20
        for i:=0; i<Matrix; i++{

                   row1=append(row1, rand.Intn(rnd))
                   row2=append(row2, rand.Intn(rnd))
                   row3=append(row3, rand.Intn(rnd))
                   
                   Summ(row1[i], row2[i], row3[i])	   
                   // fmt.Println(i)
        }

        // fmt.Println("---------",row1,row2,row3)
         
        

        // Определение размера масивов по количеству элементов 
        // в первом массиве
         
	     
  }



// func Matt(Matrix... int){

// 	for _; m:=range(Matrix) {
// 			   ss=Summ(row1[i],row2[i],row3[i])
// 			   fmt.Println(ss)
// 	}


// }


  func Summ(S... int) int {
  	var s int=0

  	for _, r:=range(S){
       s+=r
       
  	}
     
    return  s
     
  }
```



bat
```bat

SET GOPATH=%CD%

REM Запус программы
SET GOROOT=C:\GO
SET PATH=%GOROOT%\BIN;%PATH%;

rem go get -u -v github.com/dancannon/gorethink
rem go get -u -v gopkg.in/dancannon/gorethink.v1
rem go get -u -v github.com/gonum/matrix/mat64
rem go get github.com/pkg/profile

rem UNIX
rem SET GOOS=linux
rem SET GOARCH=amd64
rem SET CGO_ENABLED=0 

CLS
TITLE Run "GO" 
COLOR 0f

rem ECHO ....................................................................
REM echo gopath = %gopath%
rem ECHO ....................................................................

go build -o rgr.exe
rgr.exe

PAUSE
```



## Links 
- https://play.golang.org/p/ZdFpbahgC1  
- https://golang.org/pkg/math/rand/#example_  


