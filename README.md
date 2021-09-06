# CloudService
CloudService
1、登陆https://www.vmware.com/, 了解vmware的服务内容
运用VMware 技术奠定数位化基础，在任何云端中运用任何装置执行任何应用程式。
		混合云的优势
* 		弹性
* 		结构与区隔
尽管私有云在使用成本上(在初步的基础架构投资后) 比公有云要低许多，规模扩充却相对困难许多。要扩充基础架构的规模，就必须购买额外的设备。当私有云的使用率萎缩时，昂贵的设备将无用武之地，形成资源浪费。

2、熟悉kubernetes
￼
容器类似于 VM，但是它们具有被放宽的隔离属性，可以在应用程序之间共享操作系统（OS）。 因此，容器被认为是轻量级的。容器与 VM 类似，具有自己的文件系统、CPU、内存、进程空间等。 由于它们与基础架构分离，因此可以跨云和 OS 发行版本进行移植。
容器因具有许多优势而变得流行起来。下面列出的是容器的一些好处：
* 敏捷应用程序的创建和部署：与使用 VM 镜像相比，提高了容器镜像创建的简便性和效率。
* 持续开发、集成和部署：通过快速简单的回滚（由于镜像不可变性），支持可靠且频繁的 容器镜像构建和部署。
* 关注开发与运维的分离：在构建/发布时而不是在部署时创建应用程序容器镜像， 从而将应用程序与基础架构分离。
* 可观察性：不仅可以显示操作系统级别的信息和指标，还可以显示应用程序的运行状况和其他指标信号。
* 跨开发、测试和生产的环境一致性：在便携式计算机上与在云中相同地运行。
* 跨云和操作系统发行版本的可移植性：可在 Ubuntu、RHEL、CoreOS、本地、 Google Kubernetes Engine 和其他任何地方运行。
* 以应用程序为中心的管理：提高抽象级别，从在虚拟硬件上运行 OS 到使用逻辑资源在 OS 上运行应用程序。
* 松散耦合、分布式、弹性、解放的微服务：应用程序被分解成较小的独立部分， 并且可以动态部署和管理 - 而不是在一台大型单机上整体运行。
* 资源隔离：可预测的应用程序性能。
* 资源利用：高效率和高密度。
容器是打包和运行应用程序的好方式。在生产环境中，你需要管理运行应用程序的容器，并确保不会停机。 例如，如果一个容器发生故障，则需要启动另一个容器。如果系统处理此行为，会不会更容易？
这就是 Kubernetes 来解决这些问题的方法！ Kubernetes 为你提供了一个可弹性运行分布式系统的框架。 Kubernetes 会满足你的扩展要求、故障转移、部署模式等。

docker
Docker 使开发高效且可预测
Docker 消除了重复、平凡的配置任务，并在整个开发生命周期中用于快速、简单和可移植的应用程序开发——桌面和云。Docker 全面的端到端平台包括 UI、CLI、API 和安全性，它们旨在在整个应用程序交付生命周期中协同工作。
* 轻松交付多个应用程序，并让它们在您的所有环境中以相同的方式运行，包括设计、测试、暂存和生产 - 桌面或云原生。
* 在不同的容器中以不同的语言独立部署您的应用程序。降低语言、库或框架之间发生冲突的风险。
* 借助 Docker Compose CLI 的简单性和一个 命令，使用 AWS ECS 和 Azure ACI 在本地和云上启动您的应用程序，从而加快开发速度。
* 通过利用 Docker 映像在 Windows 和 Mac 上高效开发自己独特的应用程序，在编码方面取得领先。使用 Docker Compose 创建多容器应用程序。 
* 在整个开发流程中与您喜欢的工具集成 - Docker 可与您使用的所有开发工具配合使用，包括 VS Code、CircleCI 和 GitHub。
* 将应用程序打包为可移植容器映像，以便在从本地 Kubernetes 到 AWS ECS、Azure ACI、Google GKE 等的任何环境中一致地运行。
￼
Docker 是用Go 编程语言编写的，并利用 Linux 内核的几个特性来提供其功能。Docker 使用一种namespaces称为容器的技术来提供隔离的工作空间。当您运行一个容器时，Docker 会为该容器创建一组 命名空间。
这些命名空间提供了一层隔离。容器的每个方面都在单独的命名空间中运行，并且其访问权限仅限于该命名空间。
什么是容器？简单地说，容器只是你机器上的另一个进程，它与主机上的所有其他进程隔离开来。这种隔离利用了内核命名空间和 cgroups，这些特性已经在 Linux 中存在了很长时间。Docker 一直致力于使这些功能易于使用且易于使用。

1、docker run --nam
e repo alpine/git clone https://github.com/docker/getting-sta
rted.git(clone)

2、docker cp repo:/
git/getting-started/ .(copy to local)

3、 docker 
build -t docker101tutorial .(build the image)

4、docker run -d -p 80:80 --name docker-tutorial docker101tutorial(run)

5、docker tag docker101tutorial chengjiane2019/docker101tutorial 
      docker push chengjiane2019/docker101tutorial(save to docker hub)

6、docker info 

7、docker network 
Usage:  docker network COMMAND

Manage networks

Commands:
  connect     Connect a container to a network
  create      Create a network
  disconnect  Disconnect a container from a network
  inspect     Display detailed information on one or more networks
  ls          List networks
  prune       Remove all unused networks
  rm          Remove one or more networks

8、docker images(查看docker镜像)
      docker images docker101tutorial(列出仓库docker101tutorial中的镜像)
      docker images docker101tutorial:latest(列出仓库docker101tutorial中标签为latest的镜像)

9、docker diff 1fdfd1f54c1b(查看container1fdfd1f54c1b的变化)
  


