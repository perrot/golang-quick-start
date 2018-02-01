# go basic syntax
----
```sh
>cd C:\Go\src\mathapp
C:\Go\src\mathapp>notepad hello.go
```
//%GOROOT%\src\mathapp\hello.go
```go
package main

import "fmt"

func main() {
	fmt.Printf("Hello, world or 你好，世界 or καλημ ́ρα κóσμ or こんにちはせかい\n")
}
```
type bellow command to build the program. it will generate a hello.exe file. 
```sh
C:\Go\src\mathapp>go build hello.go
```
execute hello.exe
```sh
C:\Go\src\mathapp>hello.exe
Hello, world or 你好，世界 or καλημ ́ρα κóσμ or こんにちはせかい
```
----
```sh
>cd C:\Go\src\mathapp
C:\Go\src\mathapp>notepad type.go
```
//%GOROOT%\src\mathapp\type.go
```go
package main

import (
	"fmt" 
	"errors" 
)

var emptyString string = "<>"

func main() {
	var(
		variableName int = 1
		vstr1, vstr2 string= "v1", "v2"
	)
	vname1, vname2, vname3 := false, true, true/*use in the function only*/
	vname2=false
	_, b := 34, 35  /*same as b:=35*/

	const Pi = 3.1415926
	const i = 10000
	const (
		MaxThread = 10
		prefix = "astaxie_"
	)

	fmt.Printf("variableName : %v\n",variableName )
	fmt.Printf("vstr1: %v, vstr2: %v\n",vstr1,vstr2)
	fmt.Printf("vname1: %v, vname2: %v, vname3: %v\n",vname1,vname2,vname3)
	fmt.Printf("b : %v\n",b )

	japaneseHello := "Konichiwa"
	fmt.Printf("japaneseHello : %v\n",japaneseHello )
	fmt.Printf("emptyString : %v\n",emptyString )
	/*assign a char*/
	ch:=[]byte(japaneseHello) //convert string type to []byte type
	ch[0]='y'
	s2:=string(ch)
	fmt.Printf("s2 : %s\n",s2)

s := "hello,"
m := " world"
a := "c" +  s[1:] + m//string type can slice 
fmt.Printf("a: %s\n", a)

m1 := `hello
	world`
fmt.Printf("m1: %s\n", m1)
		var c complex64 = 5+5i
	//output: (5+5i)
	fmt.Printf("Value is: %v\n", c)

err := errors.New("emit macho dwarf: elf header corrupted")
if err != nil {
	fmt.Print(err)
}

}

```
