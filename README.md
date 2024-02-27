# Open Source Contributions

This document aims to highlight my contributions to various open-source projects that I have been involved in during my academic years. Firstly, I will provide an overview of school projects. The second part will focus on the external open-source project I contributed to: Nexth. I will detail my contribution, explaining how I approached encountered challenges and the skills I developed throughout this process.

## Kudo

- Repository: [Kudo](https://github.com/dev-sys-do/kudo)

- State of the project: experimental
- Community: not active
- Stack: Rust, Etcd, gRPC

During my first year at Polytech, I had the opportunity to work on Kudo. Although this project doesn't follow all the rules of open source, it remains open to the public, thus allowing anyone to contribute. Kudo is a container orchestrator designed to be much simpler and more accessible than Kubernetes. It's written in Rust and allows launching workloads through a CLI or an API.

My contribution to the Kudo project involved developing the HTTP API. This API aims to manage workload launch requests. I used etcd for workload storage. ETCD is a very lightweight key-value database designed to provide a reliable and fast storage mechanism for system configuration and state data. One of the major challenges encountered during this task was in serialization and deserialization of data. The process involved converting structured data in JSON format, received via the HTTP body, into strings to be stored in etcd, and vice versa. To build the necessary web server for this operation, I chose to use Actix.



## Lambdo

- Repository: [Lambdo](https://github.com/faast-rt/lambdo)

- State of the project: experimental, in development
- Community: not active
- Stack: Rust, Docker, gRPC

I also contributed to a FaaS project. FaaS is a service that allows executing pieces of code without worrying about managing the underlying infrastructure. Lambdo uses micro VMs, which can be loaded in a few hundredths of milliseconds. Unlike running code in a container, micro VMs offer increased isolation from the host kernel, thus enhancing security.

My role in Lambdo mainly involved communication with micro VMs. I was tasked with implementing a protocol for writing to and reading from the serial port. This task proved to be complex regarding retrieving information from the serial port. Additionally, I also contributed to Lambdo's documentation writing.

## Nexth

- Repository: [Nexth](https://github.com/wslyvh/nexth)
- My PR: [PR#26](https://github.com/wslyvh/nexth/pull/26)
  
- State of the project: production
- Community: active
- Stack: Next.js, Typescript, Web3


During my final year at Polytech, I contributed to Nexth, a templating project designed to provide a solid foundation for decentralized application frontend development. The project, initially based on Next.js and MUI, underwent a transition to Next.js 13, rendering existing example pages incompatible. This presented an opportunity for me to contribute by developing new example pages.

I chose to create a first page to send Ethereum, while the second facilitates ERC20 token transfer. I faced several challenges, notably due to the initial use of Wagmi v1, a library composed of React hooks facilitating interactions with the blockchain. During development, Wagmi released its version 2, introducing major changes that rendered my initial work obsolete. This forced me to rethink and rebuild the pages using the new version of Wagmi.

This experience proved to be extremely formative. Not only did it allow me to discover and become familiar with Next.js, but it also gave me the opportunity to deepen my knowledge of Wagmi, with which I already had some experience. A particularly interesting aspect of this project was optimizing transaction processing. I integrated simulations to anticipate transaction failures, thus avoiding unnecessary costs associated with transactions destined to fail.

![Nexth preview](https://raw.githubusercontent.com/Maxtho8/opensource/main/nexth-send-token.png)
