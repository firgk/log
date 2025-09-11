# error


```
遇到的一些error
```









# sqlalchemy.exc.IntegrityError: (pymysql.err.IntegrityError) (1062, "Duplicate entry '1' for key 'PRIMARY'")


```
mysql 主键不可以设置为0
```



## 302 FOUND strict-origin-when-cross-origin

```
http://127.0.0.1:8000/student/show/
请求 http://localhost:8000/student/distribution_of_actual_test_scores 报错
302 FOUND strict-origin-when-cross-origin

发现是 localhost 和 127.0.0.1 不同 所以跨域了
```

## 循环引用

```
python 中运行的一个独立的函数，终端输出，发现引用了其他的函数
循环引用了，胡乱引用了没有使用到的类或函数，但是没有使用到
编辑器会显示忽略（idea，　pycharm）但是他被加载了。

```





使用python 的 python-docx 打开文件时报错
报错命令在这一行

```
from docx import Document  
doc = Document(input_file)
```
信息
```
/firgk/Desktop/myenv/bin/python /home/firgk/Desktop/myenv/a.py
Traceback (most recent call last):
  File "/home/firgk/Desktop/myenv/a.py", line 75, in <module>
    process_table_text_in_word(input_file, output_file)
  File "/home/firgk/Desktop/myenv/a.py", line 43, in process_table_text_in_word
    doc = Document(input_file)
          ^^^^^^^^^^^^^^^^^^^^
  File "/home/firgk/Desktop/myenv/lib/python3.11/site-packages/docx/api.py", line 27, in Document
    document_part = cast("DocumentPart", Package.open(docx).main_document_part)
                                         ^^^^^^^^^^^^^^^^^^
  File "/home/firgk/Desktop/myenv/lib/python3.11/site-packages/docx/opc/package.py", line 127, in open
    pkg_reader = PackageReader.from_file(pkg_file)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/firgk/Desktop/myenv/lib/python3.11/site-packages/docx/opc/pkgreader.py", line 25, in from_file
    sparts = PackageReader._load_serialized_parts(
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/firgk/Desktop/myenv/lib/python3.11/site-packages/docx/opc/pkgreader.py", line 53, in _load_serialized_parts
    for partname, blob, reltype, srels in part_walker:
  File "/home/firgk/Desktop/myenv/lib/python3.11/site-packages/docx/opc/pkgreader.py", line 86, in _walk_phys_parts
    for partname, blob, reltype, srels in next_walker:
  File "/home/firgk/Desktop/myenv/lib/python3.11/site-packages/docx/opc/pkgreader.py", line 81, in _walk_phys_parts
    blob = phys_reader.blob_for(partname)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/firgk/Desktop/myenv/lib/python3.11/site-packages/docx/opc/phys_pkg.py", line 83, in blob_for
    return self._zipf.read(pack_uri.membername)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.11/zipfile.py", line 1517, in read
    return fp.read()
           ^^^^^^^^^
  File "/usr/lib/python3.11/zipfile.py", line 940, in read
    buf += self._read1(self.MAX_N)
           ^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/lib/python3.11/zipfile.py", line 1044, in _read1
    self._update_crc(data)
  File "/usr/lib/python3.11/zipfile.py", line 972, in _update_crc
    raise BadZipFile("Bad CRC-32 for file %r" % self.name)
zipfile.BadZipFile: Bad CRC-32 for file 'word/media/image13.jpeg'
```
这是word文件损坏了，常见于扫描的word文档






损坏的word文件，用word2021打开显示兼容性模式，解压word，发现中内嵌的图片显示CRC错误
```
C:\Users\firgk\Desktop\4、方剂学.docx
CRC 校验失败 : word\media\image86.jpeg
CRC 校验失败 : word\media\image47.jpeg
CRC 校验失败 : word\media\image91.jpeg
CRC 校验失败 : word\media\image22.jpeg
CRC 校验失败 : word\media\image73.jpeg
CRC 校验失败 : word\media\image8.jpeg
CRC 校验失败 : word\media\image85.jpeg
CRC 校验失败 : word\media\image36.jpeg
CRC 校验失败 : word\media\image42.jpeg
```




解决方法：
修复word文档
![](./src/20253101.png)
![](./src/20253102.png)



例子

(./src/方剂学_损坏文件.docx)





## 因为移动硬盘位置导致 开机出现 authentication is need to run /usr/bin 
将自己在xfce设置中添加的启动项重新添加一边（取消勾选，之后再次勾选）









## venv创建的虚拟环境失效了

原因是：移动了目录位置



需要修改pip3、activate文件
vi /home/env/pip3
将其中的路径改掉

vi /home/env/activate
将其中的路径改掉


部分版本（如python3.11) 只需要更改 activate





