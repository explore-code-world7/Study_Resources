# clamav

ClamAV 是一个开源的防病毒引擎，可以用来扫描文件，包括PDF文件。

```bash
sudo apt update
sudo apt install clamav clamtk

sudo freshclam

clamscan /path/to/your/file.pdf

clamscan -r /path/to/your/directory
```

## 异常进程处理

* 可以进一步问GPT
  
  ```bash
  ps aux | grep freshclam
  sudo killall freshclam
  ```
