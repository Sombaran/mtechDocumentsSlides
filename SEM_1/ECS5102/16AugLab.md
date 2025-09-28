# ECS5102 Lab

Co-ordinator: Sundar
> [Click here for video link](https://cciitpatna-my.sharepoint.com/personal/ecs5102_iitp_ac_in/_layouts/15/stream.aspx?id=%2Fpersonal%2Fecs5102%5Fiitp%5Fac%5Fin%2FDocuments%2FRecordings%2FECS%205102%20%2D%20Lecture%20Room%2D20250816%5F161744UTC%2DMeeting%20Recording%2Emp4&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2E60b62f23%2Da2cf%2D4aec%2D9ec3%2Dd597f76dcf24)

## Virtualization

- The foundation of cloud compution
- History
  - Assembly language
  - Machine language
  - Map hardware and software
  - Hardware: transitors electronic hardware, size of hardware started shrinking
  - Software: Made machine understand assembly language or machine understand english instruction sets
  - Sequetial code move to OOPs coding
  - Not only hardware and software were getting matued by also the business started using the computing machine
  - Commercial aspect started pushing more (money and value)
  - Utlization became key in commercial aspect becuase hardware and software got more matured
  - Assuming we are in era of 90's
  - Mainframe was technology during 90's (sharing resource time/ resource sharing)
  - Using the core technology of mainframe (sharing resource time/ resource sharing) virtualization was built
- It is small piece of software which manages hardware and create multiple machine from single resouce/server
- All these machine are virtual
- And this piece of software is called hypervisor
- Host system is the actual physical machine OS that installed the hypervisor
- Hypervisor sits on top of the OS
- Hypervisor creates VM, this VM is a bare metal which got allocated from bare metal
- This VM needs an OS, that OS is called guest OS

## Virtualization types

- Full virtualization
  - Also called bare metal/ Native
  - Removing of Host OS called type 1
  - No need to secure it, if we get rid of it
  - I cannot communicate to hardware directly
  - Production env
  - Run directly on hardware
- Para virtualization
  - Dev env
  - Generally in our laptop has type 2
