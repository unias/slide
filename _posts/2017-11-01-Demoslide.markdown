---
layout: singleslide
title:  "Pouch介绍"
date:   2017-11-30 00:45:41 -0700
categories: "slide"
---

<style type="text/css">
.floatleft{float:left;width:40%;}
.floatright{float:right;width:60%;}
</style>

<textarea id="source">

class: center, middle

# Pouch介绍

&nbsp;
&nbsp;

#### anbo
#### 2017年11月30日



---

## Pouch历史


.floatleft[
- 始于2011年，基于LXC开发的容器基础设施T4，内部使用，前身为Alidocker
- 2015年开始吸收Docker镜像功能
- 容器结合阿里内核，大幅提高隔离性
- 关键特性：安全、性能、稳定性
]
.floatright[
<img src="http://5b0988e595225.cdn.sohucs.com/images/20171127/7a9107cd9c904d67af67de89d8ea3d8c.jpeg" style="width:90%;height:90%">
]

---

## 定位

.floatleft[

- Runtime Layer
- Container Layer（位于本层，管理各种容器运行时）
- Orchestration Layer

In pouch's roadmap, we set ecosystem embracing as a big target. To upper orchestrating layer, pouch supports Kubernetes and Swarm. To underlying runtime layer, pouch is compatible with oci-compatible runtime, such as [runC](https://github.com/opencontainers/runc), [runV](https://github.com/hyperhq/runv), runlxc and so on. To make storage and network big supplements, [CNI](https://github.com/containernetworking/cni) and [CSI](https://github.com/container-storage-interface) are in scope right there.

]

.floatright[
<img src="https://github.com/alibaba/pouch/raw/master/docs/static_files/pouch_ecosystem_architecture.png" style="width:90%;height:90%">
]

---

# 架构

.floatleft[
- Pouch CLI
  - Users can interact with Pouchd by Pouch CLI.
- Pouchd
  * HTTP server
  * bridge layer
  * Manager(System/Network/Volume/Container/Image)
  * ctrd
]

.floatright[
<img src="https://github.com/alibaba/pouch/raw/master/docs/static_files/pouch_component_architecture.png" style="width:80%;height:80%">
]
---
# pouch命令

<img src="/slides/assets/images/pouch.png" style="width:90%;height:90%">
---
# Roadmap

- **Container Regular Management**

  We will polish user's experience on container management as the first important step. Moby has popularized container API standard in industry. And pouch will follow this API standard to provide container service. In addition, pouch will take more care of more aspects on how to run container on top of various isolation unit. Better experience on taking care of applications is in the scope as well.

- **Strong Isolation**

   Since security is the largest obstacle for technology to apply in production environment, pouch will improve isolation ability in the following areas: <font color=red>userspace lxcfs to isolate resource view, hypervisor based container, kvm-based container</font> and so on.

- **Open to Ecosystem**

  For being open to container ecosystem, Pouch will be designed to be scalable. As a container engine, pouch will support pod and be able to integrate upper orchestraion layer with kubernetes. For fundamental infrastructure management, pouch will embrace CNI and CSI. In the aspect of monitoring, logging and so on, Pouch takes an open role to approach cloud native.

---

class: center, middle

# 谢谢

</textarea>
