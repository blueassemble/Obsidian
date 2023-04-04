## Useful Links

-   [Packer를 사용하여 Linux Azure VM 이미지 만들기 | Microsoft Learn](https://learn.microsoft.com/ko-kr/azure/virtual-machines/linux/build-image-with-packer)
-   [Packer Azure Plugin Gihtub](https://github.com/hashicorp/packer-plugin-azure)
- 

  
  

## Azure VM Image Builder

---

1.  Builder
    1.  arm
        1.  VM 생성 및 이미지 캡처
    2.  chroot([https://en.wikipedia.org/wiki/Chroot](https://en.wikipedia.org/wiki/Chroot))
        1.  기존 VM에 연결된 관리디스크 생성 후 디스크에서 이미지 생성
2.  Auth
    1.  AAD interactive login
        1.  `use_interactive_auth`
        
    2.  Managed Identity
        
    3.  Service Principal
    4.  Azure CLI

  

## Linux

  
  

```

  

/

```