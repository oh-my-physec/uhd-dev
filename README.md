# uhd-dev

> 一个拆箱可用的 [`UHD`](https://github.com/EttusResearch/uhd) + [`GNURadio`](https://www.gnuradio.org/) Docker 环境.

### `docker/`

包含了构建 docker 镜像的脚本.

- `Dockerfile`

### `utils/`

包含了一些实用的脚本.

- `adjust-network-kernel-settings`: 使用 USRP 过程中如果出现 Warning 可以运行该脚本修改网络参数.

- `docker-run`: 帮助调用 docker 镜像内程序的脚本. 如: `docker-run uhd_usrp_probe`, `docker-run gnuradio-companion` 等.

- `matlab/`: 包含了用来读取 FileSink 文件的 MATLAB 函数.

### 构建镜像

> __Note:__ 使用本仓库前, 请确保已经浏览过 [USRP Hardware Driver and USRP Manual](https://files.ettus.com/manual/page_usrp2.html).

```bash
git clone https://github.com/oh-my-physec/uhd-dev
cd uhd-dev
docker build -t uhd-dev docker  ## 此操作需要较长时间, 请耐心等待.
```

成功执行完上述步骤后, 输入 `docker images` 查看镜像列表, 其中 `uhd-dev` 就是我们的镜像.

```                 
REPOSITORY   TAG       IMAGE ID       CREATED             SIZE
uhd-dev      latest    37148a5000c7   About an hour ago   1.86GB
```

至此, 镜像构建完成.
