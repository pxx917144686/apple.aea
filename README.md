### 下载链接 [apple.aea](https://github.com/pxx917144686/apple.aea/archive/refs/heads/main.zip)

### apple.aea [iPhone_.ipsw](https://ipsw.dev/product/iPhone)

![Preview](./xx/1.png)

### ipsw 固件，并按照大小排序，然后打开最大的 dmg.aea 文件
![Preview](./xx/2.png)

---

## 终端执行：

### 解压 `apple.aea-main.zip`

cd apple.aea-main 文件夹
```bash
cd aeota
python3 -m venv .env
source .env/bin/activate
```

## 执行aea文件夹中的 get_key.py

```bash
cd aea
python3 get_key.py <拖入 .aea 文件到终端>
```

**执行成功 ——> 得到密钥**  
例如：`'GwXUyztBvIPzXjbfcFkZ9IEBI561oI02b/nkQijCCng='`

---

## 开始解密 `.aea` 文件

### 终端执行

```bash
./
aea decrypt -i <拖入 .aea 文件到终端> -o <解密后的路径> -key-value 'base64:GwXUyztBvIPzXjbfcFkZ9IEBI561oI02b/nkQijCCng='
```


---

## 关于 制作 `iphone_.ipcc` 文件

1. 路径：`system -> library -> carrier bundles -> iphone`  
   此目录中包含众多的 `.IPCC` 文件。

```bash
**中国电信**：

ChinaTelecom_hk.bundle - 中国电信 香港
ChinaTelecom_USIM_cn.bundle - 中国电信 大陆
ChinaTelecom_USIM_mo.bundle - 中国电信 澳门

**中国移动**：

CMCC_CMI.bundle - 中国移动国际
CMCC_cn.bundle - 中国移动 大陆
CMCC_hk.bundle - 中国移动 香港
CMCC_HKBN_hk.bundle - 香港宽频

**中国联通**：

Unicom_hk.bundle - 中国联通 香港
Unicom_cn.bundle - 中国联通 大陆

```
2. 找到需要的 `.IPCC` 文件，将对应的 `xxxx.bundle` 放入新建文件夹 **Payload**。

3. 将 **Payload** 文件夹压缩为 ZIP 文件。

4. 将 ZIP 文件后缀名改为 `.ipcc`。
