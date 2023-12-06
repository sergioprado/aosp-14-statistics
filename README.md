# AOSP statistics

Test environment:

- Tests executed on AOSP 8, AOSP 13 and AOSP 14
	- aosp_x86_64-eng target used on AOSP 8
	- aosp_cf_x86_64_phone-eng target used on AOSP 13 and 14
- Built with 8 threads, 64G RAM, SATA hard disk

## Source code statistics

| Feature | AOSP 8 | AOSP 13 | AOSP 14 |
| :------ | :----: | :-----: | :-----: |
| Number of projects | 598 | 1143 | 1224 |
| Source code size | 87G | 155G | 165G |
| Lunch targets | 32 | 75 | 83 |
| Rust source files | 1009 | 6115 | 8609 |

## Build statistics

| Feature | AOSP 8 | AOSP 13 | AOSP 14 |
| :------ | :----: | :-----: | :-----: |
| Build time | 02:30 | 07:20 | 08:50 |
| Build output size | 87G | 124G | 150G |
| system.img file size | 2,5G | 935M | 688M |
| system_ext.img file size | 0 | 663M | 232M |
| vendor.img file size | 96M | 199M | 107M |
| odm.img file size | 0 | 820K | 452K |
| product.img file size | 0 | 309M | 210M |

## Migration from Makefile to Soong to Bazel

| Feature | AOSP 8 | AOSP 13 | AOSP 14 |
| :------ | :----: | :-----: | :-----: |
| Android.mk files | 3493 | 955 | 843 |
| Android.bp files | 1408 | 8660 | 9801 |
| BUILD files | 13 | 1109 | 1504 |
| *.bzl files | 6 | 494 | 821 |
| BUILD.bazel | 0 | 596 | 829 |

## Runtime statistics

| Feature | AOSP 13 | AOSP 14 |
| :------ | :-----: | :-----: |
| Kernel version | 5.15.41 | 6.1.23 |
| Number of processes | 306 | 288 |
| Number of threads | 1377 | 1332 |
| System services | 277 | 303 |
| Memory usage | 1.8G | 3.6G |
| Bootup time (soft reset until Launcher) | 1:05 | 1:20 |
| Number of APEXs | 43 | 48 |
| Number of properties | 899 | 934 |
| BPF programs in /system/etc/bpf/ | 4 | 5 |
| Default ro filesystem | ext4 | erofs |
| Default rw filesystem | ext4 | f2fs |
