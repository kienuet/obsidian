## 1. Sử dụng ed25519 thay cho rsa (do rsa thủng)
### Bước 1: Mở terminal và chạy lệnh sau để tạo SSH key
```
cd ~/.ssh
ssh-keygen -t ed25519 -C "kienntm@bkav.com" // thay mail vào đây nhé
```

### **Bước 2: Khi được hỏi, điền như sau:**

```
Enter file in which to save the key (/home/yourname/.ssh/id_ed25519): <username>
Enter passphrase (empty for no passphrase): ******** điền mk 2 lần
Enter same passphrase again: ********
```

> 💡 có thể đặt passphrase để bảo vệ key, hoặc để trống nếu không muốn nhập mỗi lần dùng.

---

## 📎 Kết quả:

Bạn sẽ có 2 file:

- `~/.ssh/kienntm(<username>)` → **private key**
    
- `~/.ssh/kienntm.pub` → **public key** (dùng để add vào server như Gerrit, GitHub...)

```
cat ~/.ssh/kienntm.pub
```

- copy publicKey 
- vào https://gerrit.bmos.bkav.com:8443/settings/#SSHKeys 
- add publicKey đã copy vào 
## 2. Nếu vẫn dùng RSA

### Bước 1: Mở terminal và chạy lệnh sau để tạo SSH key
```
cd ~/.ssh
ssh-keygen -t rsa -b 4096 -C kienntm@bkav.com // thay mail vào đây nhé
```

### Bước 2: Như trên
### Bước 3: Quan trọng
```
nano ~/.ssh/config // tạo file config cho
```

copy nội dung sau cho file config: 
```
Host gerrit.bmos.bkav.com
  HostName gerrit.bmos.bkav.com
  Port 29418
  User <username>
  IdentityFile ~/.ssh/kienntm // link privatekey
  IdentitiesOnly yes
  PubkeyAcceptedAlgorithms +ssh-rsa
```
