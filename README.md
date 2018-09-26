# CTBlockDescription
执行完class-dump之后，获得的头文件中所有的block都会写成CDUnknownBlockType
使用CTBlockDescription就可以打印出block的参数了


```
    NSMethodSignature *signature = [[[CTBlockDescription alloc]initWithBlock:arg] blockSignature];
    NSLog(@"block arg %@", [signature description]);

```

![](https://github.com/wanyawan/CTBlockDescription/blob/master/02.png)
![](https://github.com/wanyawan/CTBlockDescription/blob/master/01.png)
######分析一下三个参数：
* 第一个参数`@?` block底层调用的时候默认以block结构体自身作为第一个隐含参数 
* 第二个参数类型是NSURLSessionDataTask 
* 第三个参数是id

