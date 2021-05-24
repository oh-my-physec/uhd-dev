# uhd-dev

> 一个拆箱可用的 [`UHD`](https://github.com/EttusResearch/uhd) + [`GNURadio`](https://www.gnuradio.org/) Docker 环境.

## Usage

### 编译镜像

```bash
$ git clone https://github.com/oh-my-physec/uhd-dev
$ cd uhd-dev
$ docker build -t uhd-dev docker  ## 此操作需要较长时间, 请耐心等待.
```

成功执行完上述步骤后, `uhd-dev` 就是我们的镜像

```bash
$ docker images                    
REPOSITORY   TAG       IMAGE ID       CREATED             SIZE
uhd-dev      latest    37148a5000c7   About an hour ago   1.86GB
*******      latest    ************   ************* ago   ****GB
```

### 如何使用

本仓库提供了一个脚本 ([`docker-run`](utils/docker-run)) 供用户调用 docker 内的程序

```bash
$ docker-run uhd_usrp_probe
```

### 预装软件列表
