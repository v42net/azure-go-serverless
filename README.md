# azure-go-serverless
Quickstart: Create a Go or Rust function in Azure using Visual Studio Code
- https://learn.microsoft.com/en-us/azure/developer/go/
- https://learn.microsoft.com/en-us/azure/azure-functions/create-first-function-vs-code-other?tabs=go%2Cwindows

Remarks while trying to exactly follow the procedure as describe there:
- The workspace `Create Function` button is different (due to new version?)
- To run the function locally on Windows, run `handler.exe`
- The URL to access the local function is http://localhost:8080/api/HttpExample?name=Functions
- The terminal panel dows NOT show any information about the request

While compiling the custom handler for azure:
- As the terminal is a Powershell window:
  ```
  $Env:GOOS = "linux"
  $Env:GOARCH = "amd64"
  go build handler.go
  ```

While creating the function app in Azure:
- For the globally unique name I used `azure-go-serverless`
- For the location I used `West Europe`
- The workspace `Deploy` button is different (due to new version?)

The deployed function failed to run ... I'll troubleshoot later ...




