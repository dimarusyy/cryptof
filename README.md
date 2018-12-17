# [boost].cryptof (crypto filter)

### Overview
The class template cryptof_encryptor and cryptof_decryptor provide filtering API for encrypting/decrypting stream. 
References Crypto API on win32 and openssl on linux platform.

### Features

### Headers
> #include <boost/iostreams/filters/cryptof.hpp>

### Usage

```cpp
#include <fstream>
#include <iostream>
#include <boost/iostreams/filtering_streambuf.hpp>
#include <boost/iostreams/copy.hpp>
#include <boost/iostreams/filters/cryptof.hpp>
 
int main()
{
    std::ifstream file("hello.txt", ios_base::in | ios_base::binary);
    std::filtering_streambuf<input> in;
    in.push(boost::iostreams::cryptof::cryptof_decryptor{"private_key.pem"});
    in.push(file);
    boost::iostreams::copy(in, cout);
}
```
