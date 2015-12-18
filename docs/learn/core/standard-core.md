# AllJoyn&trade; Standard Core

## 概览
AllJoyn 框架是一个开源操作系统，为强调移动性，安全性以及动态配置的分布式应用程序提供运行环境。AllJoyn 系统可处理异构分布式 系统所固有的复杂问题，包括可移动性介入后所带来的特殊问题。借此帮助，程序开发者可以专注于解决核心问题。

AllJoyn 框架是“平台无关”的，其设计初衷为尽最大可能独立于运行设备的操作系统，硬件及软件特性。AllJoyn 框架被设计应用于 Microsoft Windows, Linux, Android, iOS, OS X, 以及 OpenWRT 平台。

亲近性与移动性一值保留在 AllJoyn 框架的设计理念当中。在移动环境中，设备会不停地进入，离开其他设备的邻域，与此同时，基础网络 容量也会发生变化。

AllJoyn SDKs 可在以下网址获得 (http://www.allseenalliance.org).

可用 AllJoyn 框架开发的应用程序类别仅仅受限于开发者的想像力。例如社交网络的拓展。用户可以建立个人简介并定义喜好和兴趣。在进入一个位置时， 支持 AllJoyn 的设备将会立即发现周边有着共同兴趣的同好，并与其建立通信网络以实现通信及信息交换。

现如今大多数设备都已集成 Wi-Fi，如此，当两名用户步入带有 Wi-Fi 热点的住宅或办公室时，他们的设备可连接到接触网络接入点，并公 开利用附加的网络容量。此外，这些设备还可以在其可见域内（取决于Wi-Fi的覆盖面积）对其他设备进行定位，同时可选择发现并使用其他 设备提供的各种服务。进一步，借助混合拓补结构，可以将一个应用了 AllJoyn Thin库的设备定义为应用蓝牙的传输机，由此便可与其他连 接到 Wi-Fi 的设备的应用程序进行交互。

另外一个例子是在实时多玩家游戏上的应用。例如，一款多玩家游戏可以运行在诸如笔记本电脑，平板电脑以及手持设备上，基础网络技术（例如 Wi-Fi）也不尽相同。这些所有的基础设施细节管理都可以经由 AllJoyn 架构处理，这使得游戏作者可以将全部精力投入游戏设计与 与实现上，而不必考虑点对点网络的复杂度。

作为 AllJoyn 生态系统的延伸， 还有很多应用程序创意。例如：

* 创建一个音乐播放列表，将歌曲共享到支持 AllJoyn 的车载音响系统中，或者将歌曲储存到家庭音响中 （受到数字版权保护）。
* 在活动或旅程结束后的的返程路上，将照片或其他媒体文件同步至支持 AllJoyn 的电视中
* 远程控制家用电器，例如电视机，数字监控系统，游戏机等。
* 在局域网内与笔记本电脑和台式机互动并分享内容。
* 在企业或教育场景中，完成同事或学生之间项目合作。
* 提供适地性服务，例如发放优惠券或 vcards. 


## AllJoyn 架构的优势

之前已提及，AllJoyn 架构是一个平台无关的系统，旨在简化分布在异构分布式系统上的邻近网络。

异构在这里不仅指代不同设备，还指运行在不同操作系统上，应用不同通信机制的不同种类的设备（例如，个人电脑，手持设备，平板电脑，消费类电子产品）。

### 开源
AllJoyn 架构一贯是开源开发。所有的 AllJoyn 代码库都开放检视并欢迎开发者进行补充和完善。如果 AllJoyn 架构缺失某一功能，你可 以添加。如果你在应用 AllJoyn 框架时遇到了困难或者技术问题，开源社区中的其他参与者会及时提供善意的帮助和指导。AllJoyn 的代码 库可以在以下网址获得 (http://www.allseenalliance.org).

### 操作系统无关性

AllJoyn 框架所提供的抽象层使其代码和应用程序可以在多种操作系统上运行。截止到本协议编写时，AllJoyn 框架已支持大多数 Linux 发行版包括 Ubuntu，并可以运行在 Android 2.3 （姜饼） 以及后续智能手机和平板电脑上。AllJoyn 框架代码也可运行在众多流行的微软 操作系统版本上，包括 Windows XP, Windows 7, Windows RT, 和 Windows 8. 此外，AllJoyn 框架代码可运行在 Apple 操作系统 iOS 以及 OS X上，以及诸如 OpenWRT 的嵌入式操作系统。

### 语言无关性

开发者目前使用 C++,Java, C#, JavaScript 以及 Objective-C 语言来创建应用程序。

### 物理网络及协议无关性

目前有许多可供联网设备使用的技术。AllJoyn 框架提供的抽象层定义了接入到基础网络站的清晰接口，使得主管软件工程师添加新的网络 实现工具变得相对容易。

例如，截止本协议编写时，Wi-Fi 联盟已经发布了支持点对点连接的 Wi-Fi Direct 技术的参数明细。Wi-Fi Direct 的网络模块正在密集的 被开发，很明显他会将 Wi-Fi Direct 以及预先关联的发现机制加入到可选网络选项中，供 AllJoyn 的开发者选择。

### 动态配置

移动设备在其寿命中常会经过多重地点，网络关联建立后又断开。这意味着 IP（Internet Protocal）地址会发生变化，网络接口会失效 ，服务也会不稳定。

当旧服务失效以及新服务出现时，AllJoyn 框架会发出提醒，如有必要也将建立新的关联。AllJoyn 框架已做好成为Wi-Fi Hotspot 2.0 （使移动电话，移动基站与 Wi-Fi 热点透明连接的技术）应用层的准备。

### 广告服务及发现
无论何时，设备的通信一定伴随着服务的推广与发现。在过去的静态网时代，设备间的通信由人工管理员做出明确的分配实现。现今时代，零配置网络的概念已十分流行，特别是借助于 Apple Bonjour 以及 Microsoft Universal Plug and Play 的帮助。

同时，我们也见到了如 Bluetooth Service Discovery Protocol 的已经存在的发现机制，以及正在发展的如 Wi-Fi Direct P2P 的发现机
制。AllJoyn 架构提供服务推广及发现的虚拟化，以简化定位及使用服务的过程。

### 安全性

在分布式应用程序中，安全性的自然模型是应用程序对应用程序的。不幸的事，在很多情况下网络安全模型并不适用于此模型。例如，蓝牙协议在完成设备配对时，会将双方设备中的所有应用程序全部授权。但如果双方设备比蓝牙耳机更复杂，如两台笔记本电脑通过蓝牙相连，这种授权模式将会变得不理想，转而需要更精细的粒度。AllJoyn 框架可对诸如此类强调应用对应用通信的复杂安全模型提供广泛支持。

### 对象模型以及远程方法调用

AllJoyn 框架应用了简单明了的对象模型以及远程方法调用（ RMI ）机制。AllJoyn 模式重新实现并扩展了 D-Bus 标准定义的有线协议，以实现对分布式设备的支持。


### 软件元件

伴随着标准化对象模型和有线协议，随之而来是将各类接口标准化为元件的能力。与 Java 接口声明机制所提供的与本地实例交互功能的实 现规范类似，AllJoyn 的对象模型提供了与编程语言无关的，与远程实现交互的规范。

有了成型的规范，就可以考虑众多接口的实现，从而使应用程序通信的标准建立变得可行。这项技术对软件组件很有帮助。软件部分是许多现代系统的中心，在类似 Android 的系统中则更为明显。在 Android 中定义了4种主要成分类型，作为仅有的能接入 Android Application Framework 的方式，同理在微软系统中，Component Object Model （ COM ）的继任版本被用作此功能。

为了实现在 [概述][overview]中所描绘的场景，我们期盼接口定义将会出现丰富的“海洋”。 AllJoyn 项目期望能与众多用户一起完成接口 的定义与标准化，并协助实现方法的共享。

## 概念性概述

AllJoyn 架构包含一系列可供使用的抽象层以便于理解并将子模块关联起来。其中只有很小部分的抽象层是理解基于 AllJoyn 的系统所必须的。

这一章提供了一个 AllJoyn 架构高层次的视角为之后的文档如 API 详解提供必要的基础。

### 远程方法调用

分布式系统是以完成同一目标为目的的使用一定形式的网络连接起来的独立计算机群，因此需要有一台机器上的一定地址空间下的某个程序以类似于本地调用的方式使用位于另一台物理分离的机器上的一个地址空间下的进程的能力。这通常是通过远程函数调用（RPC）或者以面向对象的方式来说称作远程方法调用（RMI）或远程调用（RI）的方式来完成。

RPC 的模型通常需要一个客户端也就是 RPC 的调用者和一个服务器端（AllJoyn模型中称为服务器）也就是实际上执行所期望的远程函数的 程序。调用者执行一个看上去和本地系统上的函数一样的客户端的存根，它会将函数的参数进行打包（称为对参数的编组或串行化）为某个格式的消息然后发送给 RPC 系统将其通过如传输控制协议（TCP）一类的标准机 制送达服务端。在远端机器上会有相应的 RPC 系统在运行 ，参数将会被反编组（反序列化）并将消息发送给服务端存根，它会安排执行期望的函数。如果被调用的函数需要返回任何信息，会使用相似的过程将返回值转运给客户端存根并将其发送给原始的调用者。


注意这里并没有要求一个客户端或服务端功能只能在一个进程中实现。如果两个或更多线程实现同一个客户端或服务端功能的某个方面，这些线程被看成端点。在很多情况下 AllJoyn 应用会实现类似的功能，这时它们也会被作为端点来看待。AllJoyn 架构能够支持经典的客户端 和服务器端的功能，同时也能支持端到端的网络功能。

### AllJoyn bus
AllJoyn 系统中最基本的抽象概念就是 AllJoyn 总线。它提供了一中快速轻量的方法在分布式系统中传输编组过的消息。可以将 AllJoyn 总线看成是一种消息流的“高速公路”。下图从概念上展示了一个 AllJoyn 总线在同一个设备上的实例。

![prototypical-alljoyn-bus][prototypical-alljoyn-bus]

**Figure:** Prototypical AllJoyn bus

AllJoyn 总线原理上讲包含一下几点：
 • 图中较粗的黑色横线表示总线自身，竖线可以被理解为流经总线的消息流的源头和/或目的地“出口”。
 • 与总线的连接用六边形表示。和高速公路上的出口通常会被编号类似，每一个连接会被赋予一个唯一的名字。图中使用了简化的形式来命名连接用以说明。
 • 在很多情况下到总线的连接可以被认为是和线程共驻内存的。因此，唯一连接名:1.1可能被赋予给了一个运行着某个应用实例的线程所在的连接，而唯一连接名:1.4可能被赋予给了另一个运行着某个应用实例的线程所在的连接。AllJoyn 总线的目标就是使两个应用可以在不 需要处理底层具体的交换机制的情况下进行通信。一端的连接可以被认为是客户端存根而另一端则完成所有服务端存根所要求的所有任务。

原始的 AllJoyn 总线图表达了一个 AllJoyz 总线的案例，并描绘了软件总线为接驳在其上的不同组件提供进程间通信的具体实现方法。一
般情况下， AllJoyn 总线会被延伸到下图所示的设备中。当组件需要时，一条通信链路会建立在分布在智能手机上的逻辑总线片段和分布在 Linux 主机上的组件之间。

![device-device-comm][device-device-comm]

**Figure:** 由 AllJoyn 框架操作的设备与设备间通信

此通信链路由 AllJoyn 系统管理，可以由底层技术实现，诸如 Wi-Fi 或 Wi-Fi Direct. 在 AllJoyn 主线上作为主机运行的设备可以有多
个，但对于在分布式主线上的用户这些主机是透明的。从主线的一个组件的角度看，分布式 AllJoyn 系统就像是在设备本地的一条主线。

下图展示了分布式主线在用户角度可能呈现的样子。组件（例如标签为 `:1.1`的智能手机连接）可以对标签为`:1.7`的 Linux 主机进行远
程方法调用，而无需担心该组件所处的位置。

![dist-bus-local-bus][dist-bus-local-bus]

**Figure:** A distributed AllJoyn bus appears as a local bus

### 总线路由

就像设备对设备通信图描绘的那样，逻辑分布式总线会被分为数个片段，每一片都运行在不同的设备上。在 AllJoyn 中，实现对逻辑总线分
割功能的设备被称作 AllJoyn 路由。

守护进程在由 Unix 衍生出的系统中很常见，他被用于描述为电脑系统提供重要功能性的一些程序。在 Linux 系统中我们将 daemon 称为
独立路由。在 Windows 系统中更倾向于用“服务”这个词，但我们用 AllJoyn 路由来描述他。

![总线泡泡图][bubble-diagram-bus]

**Figure:** 相关的总线泡泡图

创建泡泡图可以使 AllJoyn 路由可视化。如之前的图所示，两个 AllJoyn 总线片段分别位于智能手机和 Linux 主机上。我们用户（ C ）以及服务（ S ）来标注到总线的连接，这里用到了 RMI 中 的用户／服务理念模型。实现核心分布式总线功能的 AllJoyn 路由被标记
为 （ D ）。图中的组件被转换成下图中的图标。

![alljoyn 泡泡图][alljoyn-bubble-diagram]

**Figure:** AllJoyn 泡泡图

图中的泡泡可被看作是运行在分布式系统上的电脑进程。左边的两个用户（ C ）和服务（ S ）进程运行在智能手机上。位于右侧的路由 器用于实现在 Linux 主机上的 AllJoyn 总线的本地片段。

如分布式 AllJoyn 总线图所示，这两个路由点协调着跨越逻辑总线的消息流，呈现到连接上的则是一个整体。与智能手机端的配置相同，在 Linux 主机上同样设有两个服务组件和一个用户组件。


在这种配置中，用户组件 C1 可以对服务组件 S1 进行远程方法调用，就像操作本地对象那样一样。序列化的参数由源头被运行在智能手机上
的路由器传送出本地总线片段。经过网络链路（对用户透明）发送到 Linux 主机的路由点。Linux 主机上的 AllJoyn 路由识别出参数目的地
为 S1，随后将参数解序列化并执行远程方法调用。如果需要返回值，此进程可被反转，将返回值送回客户端。

由于独立路由运行在后台进程中，不同于用户与服务所在的进程，在每一个进程中需要有一个路由“代表”。在 AllJoyn 框架中这些代表被称
为总线附件。


### 总线附件

每一个到 AllJoyn 总线的连接都会经过特定的 AllJoyn 组件，这个组件被称作总线附件。总线附件存在于每一个需要连接到 AllJoyn 软件
总线的进程当中。

当讨论软件组件时，常会在软件和硬件之间做一个类比。分布式 AllJoyn 总线上的本地片段就像是台式机上的硬件背板总线。硬件总线可传
送电子信号，与其他卡片有被称为连接体的接驳点。类比于硬件，AllJoyn 框架中的总线附件就像硬件中的连接体。

AllJoyn 总线附件是一个已定义语言的对象，对于客户端，服务或者一个点，他代表着分布式 AllJoyn 总线。例如，C++ 语言中为用户提供
了总线附件的一种实现方法，在 Java 中则有另一种实现方法来实现同一总线附件。由于 AllJoyn 框架添加了语言联编，更多已定义语言的 实现方法将会出现。

### 总线方法，总线属性及总线信号

AllJoyn 框架是一个面向对象的系统。在面向对象的系统中，总会提及调用对象上的方法 （因此，在提及分布式系统时也常会提及远程方法
调用）。在面向对象编程理念中，对象有一系列成员。这些对象方法或属性，在 AllJoyn 框架中被称为总线方法和总线属性。AllJoyn 框架
同时还有总线信号的概念，作为在对象中一些项目或状态变化的异步提醒。

为了做到客户，服务与点之间的通信安排透明化，调用总线方法和总线信号的参数一定要有规范，同时也需要对总线属性定义一些种类信息。在计算机科学中，调用方法或信号的输入和输出的类型被称为类型签名。

类型签名由字符串定义。同时类型签名可以描述字符串，以及所有主流编程语言中的数据类型和诸如数组，结构体的复合类型。类型签名的具体任务及使用已超出了此篇简介的介绍范围。总的来说，总线方法，信号或属性的类型签名可以告知底层 AllJoyn 系统如何将传输参数和返 回值从已序列化的表达方式中转换过来。

### 总线接口

在大多数面向对象系统当中，有内在共性的方法集和属性集会被编入小组。这些功能组的统一描述被称作接口。接口是一个在实现接口规范的
实体和外界世界之间的契约。依此，接口是通过合适的标准机构的标准化的候选人。各类服务（从电话到媒体播放控制）的接口的规范可以在网站上找到。根据 D-Bus 规范，这些接口由 XML 描述。

一个接口定义将一组主线方法，主线信号和主线属性，以及他们对应的类型签名集成到一个已命名的组中。在实际操作中，接口通常由客户，服务或者点的进程实现。当已命名的接口被实现后，在实现方和外界世界之间将生成一个内含的契约，并将支持所有该接口的总线方法，总线信号及总线属性。

接口名通常取用反转的域名。例如，一个 AllJoyn 的标准接口是`org.alljoyn.Bus`接口，由路由器创建，并为总线附件提供一些基础服务。

由任意命名空间的字符串创建接口名称是不可取的。接口名称字符串为一个特定的方法服务，不可以与其他相似的字符串相混淆，尤其是主线名称。例如，`org.alljoyn.sample.chat` 可以是一个恒定不变的可以由用户搜索到的主线名称。同时也可以是一个在总线对象中定义了与已定义了总线名称的总线附件相关的，可使用的方法，信号及属性的名字。被赋予名称的接口的存在暗含在主线名称的存在当中，虽然他们有时看起来完全相同，但他们是完全不同的两类。


### 总线对象和总线路径

总线接口为工作在分布式系统上的接口的声明提供了一个标准化的方式。总线对象为实现给定规范的接口提供了脚手架。总线对象存在于总线附件中，扮演通信终点的角色。

由于实现存在于任意给定总线附件的指定接口的方法不止一种，此处需要一个可以通过对象路径实现的附加结构，用以区分这些不同的接口实现方法。

就像存在于接口命名空间的接口名字符串一样，对象路径也存在于一个命名空间中。此命名空间被规划为一个树型结构，在文件系统中寻找路径的模型则是一个目录树。事实上，对象路径的路径分隔符是一个正斜杠 (/)，与 Unix 文件系统中相同。由于总线对象是总线接口的实现，
对象路径可以与其相应接口的命名规则保持一致。

在定义磁盘控制器接口时（例如，`org.freedesktop.DeviceKit.Disks`），可以想像由下列对象路径所描述的多重实现方法，这些路径对应着两个不同的物理磁盘接口：

```sh
/org/freedesktop/DeviceKit/Disks/sda1

/org/freedesktop/DeviceKit/Disks/sda2
```

### 代理主线对象

在 AllJoyn 主线上的主线对象通过代理被访问。代理是一个可被主线访问的远端对象的本地代表。代理并不是由 AllJoyn 系统所定义的，而
是一个被广泛应用的名词。在 AllJoyn 框架中你会经常遇到 ProxyBusObject 这个词，他指示着代理的一个特定的本质－他是一个远端总线
对象的本地代理。

ProxyBusObject 是底层级 AllJoyn 代码的一部分，负责对象代理基本功能的运行。

一般情况下，RMI 系统的目的是提供一个实现接口的代理，他看起来与将调用远程对象的那一个非常相近。代理对象与远程对象实现同一个接口，但运行不同的序列化参数以及向服务发送数据的进程。

在 AllJoyn 框架中，用户与服务软件常常通过特定的编程语言联编来实现具体的用户层代理对象。用户层的代理对象则通过 AllJoyn 代理总线路径的容量来实现局部透明／远程透明的目标。

### 总线名称

AllJoyn 总线上的连接是一种用来实现被接口名所描述的接口的服务。接口的实现被整理到服务中接口总线对象的树中。用户希望通过代理对象来消费服务，这将会使用低层次 AllJoyn 代理主线对象来安排逻辑主线上主线方法，主线信号和主线属性相关信息的投递。

为了完成主线寻址步骤，与主线的连接必须有唯一标识。AllJoyn 系统为每一个主线附件分配一个临时的唯一主线标示，此唯一标识在服务每
一次连接到主线时自动生成，因此该标示并不适合作为服务的持久标识。应该有一种可以持久查阅到服务的方式，*well-known names* 被用
来充当服务的持久标示。

就像可以经域名指代在网络上的主机系统，并且在一定时间内不会变化一样，同样可以通过 well-known bus name 指代AllJoyn 主线上的功
能模块。就像接口名称是倒序的域名一样，主线名称也有此种呈现方法。由于接口名与 well-known bus names在出于方便的考虑下经常被设
定为同样的字符串，这导致了一些混淆的发生。请谨记，他们的用途完全不同：接口名定义一个由主线对象实现的，运行在主线附件中的，描述用户与服务的契约；well-known name 则指为想连接到某服务的用户提供一个稳定不变的连接方式的服务。

在应用 well-known name 时，应用程序（经过主线附件）必须事先对主线路由发出使用该标识的请求。如果此 well-known name 暂无其他用
户占用，申请者将会被给予该名称的独家使用权。该机制确保 well-known names 在任何时间都能唯一指代主线上的特定地址。

一般情况下，一个 well-known name 意味着相关的主线附件实现一系列主线对象以及一些可用服务概念的合约。由于主线名称为分布式主线
提供唯一地址，所有在主线上的主线名称必须是独特唯一。例如，`org.alljoyn.sample.chat`可用作主线名称，意味着有着相同名称的主线
附件将可实现一个聊天服务。根据该名称已被占用的事实，可以推断出在以 `/org/alljoyn/sample/chat` 为主线路径的主线对象上已经实现
了 `/org/alljoyn/sample/chat` 接口。

在实现“聊天”功能时，一方往往期望着在 AllJoyn 总线上能发现另一个同样支持聊天功能的相似组件。由于主线名称必须作为组件附件的唯
一识别，在这里就需要以加入后缀的方式确保唯一性。后缀可以是用户名，或者是一个唯一的数字。在聊天服务的例子中，可以使用多个总线附件：

```sh
org.alljoyn.sample.chat.bob

org.alljoyn.sample.chat.carol
```
此处的 well-known name 中，前缀`org.alljoyn.sample.chat.`的作用是充当服务名，可以由其推断出聊天服务接口以及对象实现的存在。后缀 `bob` and `carol` 使两个实例的 well-known name 唯一。

随之而来的问题是，处于分布式系统上的服务如何被定位。答案是通过客户端的服务广播以及发现机制。

This leads to the question of how services are located in the
distributed system. The answer is via service advertisement and discovery by clients.


### 广播及发现

关于服务广播与发现的问题主要有两方面。之前提及到，即便是对于位于 AllJoyn 总线本地片段的服务，用户仍然需要遍历所有的 well-known names来搜寻自己所需要的服务。再者，当用户试图发现并不位于现有的主线片段上的服务时，会发生更有趣的问题。

请考虑这个问题：当一方携带着运行 AllJoyn 框架的设备接近另一方的邻近场时。由于两设备已被物理分离的，框架的设备接近另一方的邻 近场时。由于两设备已被物理分离的事实，由都不可能知道对方的任何信息。那么路由点是如何确定对方设备的存在，如何判断是否有必要进行连接并建立逻辑分布式 AllJoyn 总线呢？

答案是通过 AllJoyn 服务广播和发现设备。当服务在本地设备上开始时，他首先将被赋予的 well-known name 反转，随后向他邻近域的设备
广播其存在。AllJoyn 框架提供一个抽象层，使服务可以通过底层技术，诸如Wi-Fi, Wi-Fi Direct 或其他未来的无线传输方式来实现透明广
播。

例如，在一个联系人交换应用程序中，其中的一个实例可以将 well-known name：`org.alljoyn.sample.contacts.bob` 反转并广播。如此
做将触发以下一种或多种事件：通过 Wi-Fi 接入点进行 UDP 组播，通过 Wi-Fi Direct 进行预关联服务的广播，或者通过蓝牙服务发现协议
发送消息。广播的通信机制并不需要考虑广播者。由于联系人交换在概念上是一个点对点的应用程序，一方通常会希望另一方也广播类似的交换服务，例如 `org.alljoyn.sample.contacts.carol`.

应用程序客户端也可通过初始化一个发现操作来声明他们对接收广播的兴趣所在。例如，用户可以要求添加前缀为`org.alljoyn.sample.contacts`的联系人服务实例。若如此做，两方设备都会发出这种请求。

底层 AllJoyn 系统在移动电话进入其他设备的邻近域时立即开始通过可用传输渠道传输并接受广播。每台设备在相应服务可使用时也会收到提醒。

由于服务推广可以通过多种传输方式接受，在某些情况里还需要附加的底层工作以便生成底层通信机制，对已发现服务的应用还有另外一部分概念。这就是通信会话。

### 会话

关于总线名称，对象路径以及接口名成的概念已经被讨论过。回想一下，实体连接到 AllJoyn 总线后会被分配一个唯一的标识。连接（主线
附件）也可申请一个 well-known name. 此 well-known name 可被用户用于定位或发现总线上的服务。例如，一个服务可以连接到 AllJoyn 总线上并被分配唯一识别符 `:1.1`. 如果服务希望他可以被其他在总线上的实体找到，此服务必须从总线申请一个 well-known name，例如
`com.companyA.ProductA`（后面常会加上一个唯一的实体限定符）。

此识别符至少指示一个实现了一些 well-known interface 的总线对象。一般情况下，在连接实例内，总线对象可以被一个与 well-known name 包含相同组件（此处并非是强制要求，仅仅是为了方便）的路径辨认出来。在这个例子中，对应总线识别符`com.companyA.ProductA`
的路径可以是`/com/companyA/ProductA`.


为了明白用户总线附件到相似的服务附件之间的通信会话的形成机制，也为了提供一个终端到终端的例子，我们可以将 AllJoyn 机制与一个
类似的机制做一下比对。

#### 邮政地址的类比

在 AllJoyn 框架中，服务会请求一个对人类可读的名字，以便于将自己以众所周知的，简单易懂的标签广播出去。为了底层网络中消息交换的正常运转，Well-known names 一定需要被翻译成唯一的标识，例如：

```
Well-known-name:org.alljoyn.sample.chat

Unique name::1.1
```

这里我们得知，被以`org.alljoyn.sample.chat`广播的 well-known name 对应着已被分配唯一标识 `:1.1` 的总线附件。这种方式类似于有
着名字和邮寄地址的生意。继续类比：此生意很可能会存在于同时有着其他生意的建筑中。在这种情况下，这个生意的地址可能会被一个更具体的房间号所描述。由于 AllJoyn 总线附件可以提供不止一个服务，这里一定也有可以识别多个在给定附件上的目的地址的方法。“ contact port numbe ”就对应着邮寄地址类比中的房间号。

就像人们在发送信件时可以选择使用国家邮件系统（例如美国邮政局，法国邮政局），也可以使用私人公司（联邦快递，联合包裹服务公司），同时还可以选择紧急程度（次日达，两工作日，），在使用 AllJoyn 框架联系服务时，使用者必须明确提出想获取的网络连接的特性（
例如，可靠送达的消息，可靠送达并未经排列的消息，不可靠送达并未经排列的消息）以便提供详尽的配送规范。

请注意以上例子中地址信息的分隔以及信息的投递。同理于用户可考虑在诸多快递方式中选择一种完成信件传送，用户也可以在 AllJoyn 系统中选择一种方式完成数据传送。

#### AllJoyn 会话

与一封规范列出“寄出地”和“目的地”地址的信同理，AllJoyn 会话也需要与“寄出地”和“目的地”相等价的信息。在 AllJoyn 系统中，寄出地地址对应着用户组件的位置，目的地地址则对应服务的位置。

严格地说，这些地址在电脑网络中应该被成为 half-associations. 在 AllJoyn 框架中，收件人（服务端）地址通常是如下形式的：
```c
{session options, bus name, session port}
```

第一个区域是会话选项，决定着数据的传送方式。在 IP 网络中，会话选项可以使 TCP 或者 UDP. 在 AllJoyn 框架中这些细节会被虚拟化，
对应的选项则会变为“基于消息的”，“未排列的数据”，或者“不稳定的未排列数据”。服务的目的地由相关主线附件所请求的 well-known name 给出。

与之前邮编地址例子中的�房间号类似，AllJoyn 模型中也有在主线附件“里面”的传送点概念。此概念在 AllJoyn 框架中被称为会话端口。房
间号只有在给定建筑内才有意义，会话端口号同理，必须要在给定的总线附件范围内定义。联系端口的存在与数值被主线标识所间接指出，这与底层的对象和接口组被间接指出的方式相同。

寄件人地址对应客户端信息，也是由相似的原理生成。为了和服务端正常通信，客户端必须有自己的 half-association.

```c
{session options, unique name, session ID}
```
客户端不需要申请 well-known 主线名称，所以他们可以提供自己的唯一标识符（例如`:1.1`）。由于客户端不是会话的终点，他们也不需要提供会话端口，但是在连接建立完成后会被分配会话 ID. 在会话建立步骤中此会话 ID 也会被返回到服务器端。对于熟悉 TCP 网络结构的人
，此操作与 TCP 中建立连接的操作是对等的，服务器端通过 well-known 端口被访问。在会话建立后，客户端用一个临时端口描述相似的 half-association.

在建立会话时，两方的 half-associations 会被聚合：

```c
{session options, bus name, session port}	Service

{session options, unique name, session ID}	Client
```
注意，会话选项中有两个选择。在通信建立时，会话机制被看作是服务端所能提供的会话选项以及由客户端所请求的会话选项。在会话建立过程中，有一部分是用来协商何种会话选项将会最终被采取。一旦会话建立完成，两方的 half-associations 会生成一个唯一的 AllJoyn 通信路径：

```c
{session options, bus name, unique name, session ID}
```

在会话建立程序中，两个正在通信的路由节点之间会形成一个逻辑网络连接。这将会形成一个 wireless radio topology management operation. 如果以上连接已经存在，他将会被再次使用。新创建的底层路由对路由连接被用来完成初始安全检查，检查完成后两路由就已成功将两个原本分离的 AllJoyn 软件主线片段聚合成为一个更大一些的虚拟主线。

由于在某些技术中，有关终端对终端的底层连接流量控制一定要用拓扑学考虑使其均衡化，两个终端实际的连接（“寄件人”客户端和“收件人”服务端）可能也可能不会导致另一个独立的通信信道被创建。

在某些情况中，经过 ad hoc 拓扑结构传送信息会较为方便，而在另外一些情况下通过一个新连接 （TCP/IP）进行直接传送比较方便。这种
情况下需要对底层技术有深入的了解，AllJoyn 框架很乐意为你完成这一点。用户所要做的仅仅是确保消息通过某种传送机制根据应用程序的 抽象需求被正确的转发。

#### 自我加入功能

在 AllJoyn R14.06 的版本之前，应用程序无法参与由自己作主机的会话。

In AllJoyn releases up to R14.06, it was impossible for applications
to join a session they themselves hosted. For applications that consume
information or services they themselves also provide, this created an
asymmetry: they had to treat the bus objects they hosted themselves
differently from those hosted by other peers. The self-join feature
removes this asymmetry by allowing applications to join the sessions
they themselves host. Consequently, a locally hosted bus object can be
treated in exactly the same way as a remotely hosted bus object.

#### Determining the presence of a peer - pinging and auto-pinging

Sometimes, a application needs to know which peers are present on the communication
channel ("the wire") and which aren't.  For this reason, a PING API was introduced in
version 14.06. This PING API allows to determine whether a peer is up or not.
However, for this API, the responsibility for using the PING API was with the
Application, which periodically needed to ping the peers. From Release 14.12 onwards,
an automatic PING or Auto-Pinger is introduced. This Auto-Pinger performs the
periodic peer detection, relieving  the application of having to do it.

### Bringing it all together

The AllJoyn framework aims to provide a software bus that
manages the implementation of advertising and discovering services,
providing a secure environment, and enabling location-transparent
remote method invocation. A traditional client/service arrangement
is enabled, and peer-to-peer communications follow by combining
the aspects of client and services.

The most basic abstraction in the AllJoyn framework is the
software bus that ties everything together. The virtual distributed
bus is implemented by AllJoyn routing nodes which are background
programs running on each device. Clients and services (and peers)
connect to the bus via bus attachments. The bus attachments
live in the local processes of the clients and services and
provide the interprocess communication that is required to
talk to the local AllJoyn router.

Each bus attachment is assigned a unique name by the system
when it connects. A bus attachment can request to be granted
a unique human-readable bus name that it can use to advertise
itself to the rest of the AllJoyn world. This well-known bus
name lives in a namespace that looks like a reversed domain
name and encourages self-management of the namespace.
The existence of a bus attachment of a specific name implies
the further existence of at least one bus object that implements
at least one interface specified by a name. Interface names are
assigned out of a namespace that is similar, but has a different
meaning than bus names. Each bus object lives in a tree structure
rooted at the bus attachment and described by an object path
that looks like a Unix filesystem path.

The following figure shows a hypothetical arrangement of how
all of these pieces are related.

![hypothetical-alljoyn-bus-instance][hypothetical-alljoyn-bus-instance]

**Figure:** Overview of a hypothetical AllJoyn bus instance

At the center is the dark line representing the AllJoyn bus.
The bus has "exits" which are the BusAttachments assigned
the unique names `:1.1` and `:1.4`. In the figure, the BusAttachment
with the unique name of `:1.1` has requested to be known as
`org.alljoyn.samples.chat.a` and has been assigned the corresponding
well-known bus name. The "a" has been added to ensure that
the bus name is unique.

There are a number of things implied by taking on that bus name.
First, there is a tree structure of bus objects that resides
at different paths. In this hypothetical example, there are
two bus objects. One is at the path `/org/alljoyn/samples/chat/chat`
and which presumably implements an interface suitable for chatting.
The other bus object lives at the path `/org/alljoyn/samples/chat/contacts`
and implements an interface named `org.alljoyn.samples.chat.contacts`.
Since the given bus object implements the interface, it must
provide implementations of the corresponding bus methods,
bus signals, and bus properties.

The number 42 represents a contact session port that clients
must use to initiate a communication session with the service.
Note that the session port is unique only within the context of
a particular bus attachment, so the other bus attachment in the
figure may also use 42 as its contact port as shown.

After requesting and being granted the well-known bus name,
a service will typically advertise the name to allow clients
to discover its service. The following figure shows a service making an
advertise request to its local router. The router, based on
input from the service, decides what network medium-specific
mechanism it should use to advertise the service and begins doing so.

![service-performs-advertise][service-performs-advertise]

**Figure:** Service performs an Advertise

When a prospective client wants to locate a service for consumption,
it issues a find name request. Its local router device, again
based on input from the client, determines the best way to
look for advertisements and probes for advertisements.

![client-requests-find-name][client-requests-find-name]

**Figure:** Client requests to Find Name

Once the devices move into proximity, they begin hearing
each other's advertisements and discovery requests over whichever
media are enabled. The following figure shows how the router hosting the
service hears the discovery requests and responds.

![router-reports-found-name][router-reports-found-name]

**Figure:** Router reports Found Name

Finally, the following figure shows the client receiving an indication
that there is a new router in the area that is hosting the desired service.

![client-discovers-service][client-discovers-service]

**Figure:** Client discovers service

The client and service sides of the developing scenario both
use methods and callbacks on their bus attachment object to
make the requests to orchestrate the advertisement and discovery
process. The service side implements bus objects to provide
its service, and the client will expect to use a proxy object
to provide an easy-to-use interface for communicating with
the service. This proxy object will use an AllJoyn ProxyBusObject
to orchestrate communication with the service and provide
for the marshaling and unmarshaling of method parameters
and return values.

Before remote methods can be called, a communication session
must be formed to effectively join the separate bus segments.
Advertisement and discovery are different from session establishment.
One can receive an advertisement and take no action. It is
only when an advertisement is received, and a client decides
to take action to join a communication session, that the
buses are logically joined into one. To accomplish this,
a service must create a communication session endpoint and
advertise its existence; and a client must receive that
advertisement and request to join the implied session.
The service must define a half-association before it advertises
its service. Abstractly this will look something like the following:

```c
{reliable IP messages, org.alljoyn.samples.chat.a, 42}
```

This indicates that it will talk to clients over a reliable
message-based transport, has taken the well-known bus name
indicated, and expects to be contacted at session port 42.
This is the situation seen in the hypothetical bus instance figure.

Assume that there is a bus attachment with the unique
name `:2.1` wanting to connect from a physically remote
routing node. It will provide its half association to the
system and a new session ID will be assigned and communicated
to both sides of the conversation:

```c
{reliable IP messages, org.alljoyn.samples.chat.a, :2.1, 1025}
```

The new communication session will use a reliable messaging
protocol implemented using the IP protocol stack which will
exist between the bus attachment named `org.alljoyn.samples.chat.a`
(the service) and the bus attachment named :2.1 (the client).
The session ID used to describe the session is assigned by
the system and is 1025 in this case.

As a result of establishing the end-to-end communication
session, the AllJoyn system takes whatever actions are
appropriate to create the virtual software bus shown in
the distributed bus figure. Note that this is a virtual picture, and what
may have actually happened is that a Wi-Fi Direct peer-to-peer
connection was formed to host a TCP connection, or a Wireless
access point was used to host a UDP connection, depending
on the provided session options. Neither the client nor
the service is aware that this possibly very difficult
job was completed for them.

At this point, authentication can be attempted if desired
and then the client and service begin communicating using the RMI model.

Of course, the scenario is not limited to one client on one
device and one service on another device. There may be any number
of clients and any number of services (up to a limit of device or
network capacity) combining to accomplish some form of
cooperative work. Bus attachments may take on both client
and service personalities and implement peer-to-peer services.
AllJoyn routers take on the hard work of forming a manageable
logical unit out of many disparate components and routing messages.
Additionally, the nature of the interface description and
language bindings allow interoperability between components
written in different programming languages.

## High-Level System Architecture

From the perspective of a user of the AllJoyn system, the most
important piece of the architecture to understand is that of
a client, service, or peer. From a system perspective, there
is really no difference between the three basic use cases;
there are simply different usage patterns of the same system-provided functionality.

### Clients, services, and peers

The following figure shows the architecture of the system from a user
(not AllJoyn router) perspective.

![client-service-peer-arch][client-service-peer-arch]

**Figure:** Basic client, service, or peer architecture

At the highest level are the language bindings. The AllJoyn system
is written in C++, so for users of this language, no bindings
are required. However, for users of other languages, such
as Java or JavaScript, a relatively thin translation layer
called a language binding is provided. In some cases, the binding
may be extended to offer system-specific support. For example,
a generic Java binding will allow the AllJoyn system to be
used from a generic Java system that may be running under
Windows or Linux; however, an Android system binding may
also be provided which more closely integrates the AllJoyn system
into Android-specific constructs such as a service component in
the Android application framework.

The system and language bindings are built on a layer of helper
objects which are designed to make common operations in the
AllJoyn system easier. It is possible to use much of the AllJoyn
system without using these helpers; however, their use is
encouraged since it provides another level of abstract interface.
The bus attachment, mentioned in the previous chapters, is a
critical helper without which the system is unusable. In addition
to the several critical functions provided, a bus attachment
also provides convenience functions to make management of
and interaction with the underlying software bus much easier.

Under the helper layer is the messaging and routing layer.
This is the home of the functionality that marshals and
unmarshals parameters and return values into messages that
are sent across the bus. The routing layer arranges for the
delivery of inbound messages to the appropriate bus objects
and proxies, and arranges for messages destined for other
bus attachments to be sent to an AllJoyn router for delivery.

The messaging and routing layer talks to an endpoint layer.
In the lower levels of the AllJoyn system, data is moved
from one endpoint to another. This is an abstract communication
endpoint from the perspective of the networking code.
Networking abstractions are fully complete at the top of the
endpoint's layer, where there is essentially no difference
between a connection over a non Wi-Fi radio (Bluetooth) and
a connection over a wired Ethernet.

Endpoints are specializations of transport mechanism-specific
entities called transports, which provide basic networking
functionality. In the case of a client, service, or peer,
the only network transport used is the local transport.
This is a local interprocess communication link to the
local AllJoyn bus router. In Linux-based systems, this is
a Unix-domain socket connection, and in Windows-based systems
this is a TCP connection to the local router.

The AllJoyn framework provides an OS abstraction layer to
provide a platform on which the rest of the system is built,
and at the lowest level is the native system.

### Routers

AllJoyn routers are the glue that holds the AllJoyn system together.
As previously discussed, routers are programs that run in
the background, waiting for interesting events to happen and
responding to them. Because these events are usually external,
it is better to approach the router architecture from a bottom-up
perspective.

At the lowest level of the router architecture figure below,
resides the native system. We use the same OS abstraction layer
as we do in the client architecture to provide common abstractions
for routers running on Linux, Windows, and Android. Running on
the OS abstraction layer, we have the various low-level networking
components of the router. Recall that clients, services, and
peers only use a local interprocess communication mechanism
to talk to a router, so it is the router that must deal with
the various available transport mechanisms on a given platform.
Note the "Local" transport in the router architecture figure which is the sole
connection to the AllJoyn clients, services, and peers running
on a particular host.

![router-arch][router-arch]

**Figure:** Basic router architecture

For example, a Bluetooth transport would handle the complexities
of creating and managing piconets in the Bluetooth system.
Additionally, a Bluetooth transport provides service advertisement
and discovery functions appropriate to Bluetooth, as well
as providing reliable communications. Bluetooth and other
transports would be added at this transport layer along side
the IP transport.

The wired, Wi-Fi, and Wi-Fi Direct transports are grouped under
an IP umbrella since all of these transports use the underlying
TCP-IP network stack. There are sometimes significant differences
regarding how service advertisement and discovery is accomplished,
since this functionality is outside the scope of the TCP-IP
standard; so there are modules dedicated to this functionality.

The various technology-specific transport implementations are
collected into a Network Transports abstraction. The Sessions module
handles the establishment and maintenance of communication
connections to make a collection of routers and AllJoyn applications
appear as a unified software bus.

AllJoyn routers use the endpoint concept to provide connections
to local clients, services, and peers but extend the use of
these objects to bus-to-bus connections which are the transports
used by routers to send messages from host-to-host.

In addition to the routing functions implied by these connections,
an AllJoyn router provides its own endpoints corresponding
to bus objects used for managing or controlling the software
bus segment implemented by the router. For example, when
a service requests to advertise a well-known bus name, what
actually happens is that the helper on the service translates
this request into a remote method call that is directed to
a bus object implemented on the router. Just as in the case
of a service, the router has a number of bus objects living
at associated object paths which implement specific named interfaces.
The low-level mechanism for controlling an AllJoyn bus is
sending remote method invocations to these router bus objects.

The overall operation of certain aspects of router operation
are controlled by a configuration subsystem. This allows a
system administrator to specify certain permissions for the
system and provides the ability to arrange for on-demand
creation of services. Additionally, resource consumption may
be limited by configuration of the router, allowing a system
administrator to, for example, limit the number of TCP connections
active at any given time. There are options which allow system
administrators to mitigate the effects of certain denial-of-service
attacks, by limiting the number of connections which are
currently authenticating, for example.

## Summary

The AllJoyn framework is a comprehensive system designed to
provide a framework for deploying distributed applications
on heterogeneous systems with mobile elements.

The AllJoyn framework provides solutions, building on proven
technologies and standard security systems, that address the
interaction of various network technologies in a coherent,
systematic way. This allows application developers to focus
on the content of their applications without requiring a large
amount of low-level networking experience.

The AllJoyn system is designed to work together as a whole
and does not suffer from inherent impedance mismatches that
might be seen in ad-hoc systems built from various pieces.
We believe that the AllJoyn system can make development and
deployment of distributed applications significantly simpler
than those developed on other platforms.

[overview]: #overview
[prototypical-alljoyn-bus]: /files/learn/standard-core/prototypical-alljoyn-bus.png
[device-device-comm]: /files/learn/standard-core/device-device-comm.png
[dist-bus-local-bus]: /files/learn/standard-core/dist-bus-local-bus.png
[bubble-diagram-bus]: /files/learn/standard-core/bubble-diagram-bus.png
[alljoyn-bubble-diagram]: /files/learn/standard-core/alljoyn-bubble-diagram.png
[hypothetical-alljoyn-bus-instance]: /files/learn/standard-core/hypothetical-alljoyn-bus-instance.png
[service-performs-advertise]: /files/learn/standard-core/service-performs-advertise.png
[client-requests-find-name]: /files/learn/standard-core/client-requests-find-name.png
[router-reports-found-name]: /files/learn/standard-core/router-reports-found-name.png
[client-discovers-service]: /files/learn/standard-core/client-discovers-service.png
[client-service-peer-arch]: /files/learn/standard-core/client-service-peer-arch.png
[router-arch]: /files/learn/standard-core/router-arch.png
