<div align="center">
   <a href="https://github.com/WELL-E/AutoUpdater">
     <img alt="JC Update" width="200" heigth="200" src="https://raw.githubusercontent.com/WELL-E/AutoUpdater/master/img/jc_update_new.png"></img>
   </a>
 <p>
    This is a Wpf-based automatic update application to help developers better complete the update function.
  </p>
</div>


---------------

### Description:

WPF & MVVM

- Support for update package file verification (comparison file MD5 code) 
- Support for distinguishing between x86 and x64 programs
- Support for the version number of the updater
- Support for performing update strategies

### Usage:

Program startup requires 6 parameters

1. Current version number (0.9.0.0)
2. Upgraded version number (1.0.0.0)
3. Update description URL (https://github.com/WELL-E)
4. Update package file URL（ http://localhost:9090/UpdateFile.zip）
5. Updated file release path (E:\PlatformPath)
6. Update package file MD5 code (2b406701f8ad92922feb537fc789561a)

For parameters such as debugging, the parameters can be set to：`0.9.0.0 1.0.0.0 https://github.com/WELL-E http://localhost:9090/UpdateFile.zip E:\PlatformPath 2b406701f8ad92922feb537fc789561a`

**annotate：** `http://localhost:9090/UpdateFile.zip`

- `http://localhost:9090/`：File server address built for yourself
- UpdateFile.zip：Update package file name

If you have any questions，QQ Group:130108655

### Screenshots:

![](http://i.imgur.com/oWcbNhb.png)

### Special thanks:
@[JusterZhu](https://github.com/JusterZhu)

### Acknowledgements:

- MahApps.Metro: [https://github.com/MahApps/MahApps.Metro](https://github.com/MahApps/MahApps.Metro "https://github.com/MahApps/MahApps.Metro")
- Source of software icon: [https://www.iconfinder.com/icons/314711/cloud_download_icon#size=128](https://www.iconfinder.com/icons/314711/cloud_download_icon#size=128 "https://www.iconfinder.com/icons/314711/cloud_download_icon#size=128")

### License:

Open sourced under the MIT license.

### 使用方法
  
  
        string ClientProcessName= AppDomain.CurrentDomain.BaseDirectory + "AutoUpdater.exe"          
        Process process = new Process();
            string currentVersion = "2.0.0.1";
            string newVersion = "2.0.0.1";
            string UpdateLogUrl = "http://172.6.65.167/newLog.txt";
            string UpdateFileUrl = "http://172.6.65.167/Debug.zip";
            string unpackPath =AppDomain.CurrentDomain.BaseDirectory;
            process.StartInfo.FileName = ClientProcessName;
            process.StartInfo.UseShellExecute = false;
            process.StartInfo.CreateNoWindow = true;
            process.StartInfo.Arguments = $"{ currentVersion} {newVersion} {UpdateLogUrl} {UpdateFileUrl} {unpackPath} xx";
            process.Start();

