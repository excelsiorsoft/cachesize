#CPU Cache Information for Java


This library provides access to CPU cache information in Java. The goal is to enable the development of cache aware algorithms in Java.

Currently only Intel processors are supported. The library is available for the following operating systems : 

* Linux 32/64 bits 
* Windows 32/64 bits 
* Mac OSX 64 bits

The C/ASM source of the JNI library is included in the source code, so feel free to compile for other platforms.

#Getting Started

Cachesize is available from Maven Central : 

```
<dependency> 
<groupId>fr.ujm.tse.lt2c.satin</groupId> 
<artifactId>cachesize</artifactId> 
<version>0.2.1</version> 
</dependency>
```

 ###Retrieving total size of the L1 instruction cache and the line size of the L1 data cache : 
```
CacheInfo info = CacheInfo.getInstance(); 

int cacheL1InstructionTotalSize =info.getCacheSize(CacheLevel.L1, CacheType.INSTRUCTION_CACHE); 

int cacheL1DataLineSize =info.getCacheLineSize(CacheLevel.L1, CacheType.DATA_CACHE); 
```
