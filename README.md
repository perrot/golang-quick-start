# golang-quick-start
0. the environment: go1.9.3.windows-amd64.msi, windows 10.
----

1. win+r then input "cmd" to start command prompt. type "systeminfo" to check the system type.
2. the system type is x64-based PC. download windows-amd64 from http://golang.org/dl/.
3. install windows-amd64.exe. click all next button. install to the default path.
4. "echo %GOROOT%" to print the go env variable in the console.
5. create a sample
```sh
cd %GOROOT%/src
mkdir mymath
notepad sqrt.go
```
```go
// %GOROOT%/src/mymath/sqrt.go
package mymath

func Sqrt(x float64) float64 {
	z := 0.0
	for i := 0; i < 1000; i++ {
		z -= (z*z - x) / (2 * x)
	}
	return z
}
```
6. **compile and install package sqrt.go (go install) **
```sh
C:\Go>cd %GOROOT%\src\mymath

C:\Go\src\mymath>go install
```
7. it will generate a applicatoin package to the directory C:\Go\pkg\windows_amd64\mymath.a

8. edit main.go
```sh
cd %GOROOT%/src
mkdir mathapp
cd mathapp
notepad main.go
```
//$GOPATH/src/mathapp/main.go
```go
package main

import (
	"mymath"
	"fmt"
)

func main() {
	fmt.Printf("Hello, world.  Sqrt(2) = %v\n", mymath.Sqrt(2))
}
```
9.** compile the program main.go (go build).** it will generate a executable file under the current folder.
```sh
C:\Go\src\mathapp>**go build**
```
10. execute the program mathapp.exe.
```sh
C:\Go\src\mathapp>mathapp.exe
Hello, world.  Sqrt(2) = 1.414213562373095
```
