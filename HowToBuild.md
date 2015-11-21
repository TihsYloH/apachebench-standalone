#_How to build this project._

# Introduction #

This page describe how to build ab from apachebenche-standalone.


# Download source code #

You can get the source code from the svn repository. Please follow the instruction on [source](http://code.google.com/p/apachebench-standalone/source) page to check it out.

For end users, the best way is to download a release source package from our [download](http://code.google.com/p/apachebench-standalone/downloads/list) page.

# Depend packages #

This project depends on Apache Portable Runtime library and APR-util library, they must be available in your system before building this project.Following are information for Ubuntu 8.10 distributions. Other distributions should be the same.

Before starting, please check to see if there is a more up-to-date version available to download. Visit http://apr.apache.org/ to find out about the available versions.

The following struction shows you how to install Apache Portable Runtime(apr) Library on Ubuntu Linux system. **Note:** Replace 1.3.3 with your version number:

  * Downloading apr:
```
    wget -c http://apache.mirror.phpchina.com/apr/apr-1.3.3.tar.gz
```

  * Extracting files from the downloaded package:
```
    tar -jxvf apr-1.3.3.tar.bz2
```

  * Enter the directory where the package is extracted.
```
    cd apr-1.3.3
```

  * Configuring apr Library:
```
    configure
```

  * Compiling apr:
```
    make; 
```

  * Installing apr:
```
    sudo make install
```

  * Create a soft link to apr pkgconfig file.
```
    sudo ln -s /usr/local/apr/lib/pkgconfig/apr-1.pc /usr/local/lib/pkgconfig/apr-1.pc 
```


  * Compile apr-skeleton.c to test if apr lib is installed successfully.
```
    cd apachebench-standalone
    make apr-skeletion
```



The following struction shows you how to install Apache Portable Runtime Utility (apr-util) Library on Ubuntu Linux system.**Note:** Replace 1.3.4 with your version number:

  * Downloading
```
    wget -c http://apache.mirror.phpchina.com/apr/apr-util-1.3.4.tar.bz2
```

  * Extracting files from the downloaded package:
```
    tar -jxvf apr-util-1.3.4.tar.bz2    
```

  * Configuring apr-util Library:
```
    ./configure --with-apr=/usr/local/apr
```

  * Compiling apr-util:
```
    make
```

  * Installing apr-util:
```
    make install
```


# compile #

Download or check out source code.

Enter source code directory:

```
    make ab
```



# Reference #

  * [Installing Apache Portable Runtime (apr) Library on Ubuntu Linux](http://www.techsww.com/tutorials/libraries/apr/installation/installing_apache_portable_runtime_library_on_ubuntu_linux.php)

  * [Installing Apache Portable Runtime Utility (apr-util) Library on Ubuntu Linux](http://www.techsww.com/tutorials/libraries/apr-util/installation/installing_apache_portable_runtime_utility_library_on_ubuntu_linux.php)