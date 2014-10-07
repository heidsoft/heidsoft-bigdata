#Cloudera’s VM
	These virtual machines make it easy to get started with CDH (
	Cloudera’s 100% open source Hadoop platform that includes 
	Impala, Search, Spark, and more) and Cloudera Manager. 
	They come complete with everything you need to learn Hadoop.

#Important
	These are 64-bit VMs. They requires a 64-bit host OS and a virtualization product that can support a 64-bit guest OS.
	To use a VMware VM, you must use a player compatible with WorkStation 8.x or higher: 
	Player 4.x or higher, ESXi 5.x or higher, or Fusion 4.x or higher. 
	Older versions of WorkStation can be used to create a new VM using the same virtual disk (VMDK file),
	but some features in VMware Tools won't be available.
	The VM and file size vary according to the CDH version as follows:

	CDH and Cloudera Manager Version	VM Size	File Size
	CDH 5 and Cloudera Manager 5	8 GB	3 GB

#CDH 5	
	To learn more about CDH 5, see the CDH 5 documentation.
	For the latest important information about new features, incompatible changes, and known issues in CDH 5, see the CDH 5 Release Notes.
	For information on the versions of the components in the latest release of CDH 5, and links to each project's changes files and release notes, see the packaging section of CDH Version and Packaging Information.
	Cloudera Manager 5
	As part of the boot process, the VM automatically launches Cloudera Manager and configures Flume, HBase, HDFS, Hive, Hue, Impala, Key-Value Store Indexer, Oozie, Solr, Sqoop, Spark, YARN, and ZooKeeper services. Only the HDFS, Hive, Hue, YARN, and ZooKeeper services are started automatically. The remaining services are not automatically started to conserve RAM but can be launched manually.
	You can start or reconfigure any installed services using Cloudera Manager, which is automatically displayed when the VM starts. Standard CDH 5 command-line tools are available for use as well.
	For more information about Cloudera Manager including installation, configuration, and usage instructions, see the Cloudera Manager 5 documentation.

#Accounts
	Once you launch the VM, you are automatically logged in as the cloudera user. The account details are:
	username: cloudera
	password: cloudera
	The cloudera account has sudo privileges in the VM. The root account password is cloudera.
	Hue and Cloudera Manager use the same credentials.

##QuickStart VMware Image
	To launch the VMware image, you will either need VMware Player for Windows and Linux, or VMware Fusion for Mac. Note that VMware Fusion only works on Intel architectures, so older Macs with PowerPC processors cannot run the QuickStart VM.

##QuickStart VirtualBox Image
	Some users have reported problems running CentOS 6.2 in VirtualBox. If a kernel panic occurs while the VirtualBox VM is booting, you can try working around this problem by opening the Settings > System > Motherboard tab, and selecting ICH9 instead of PIIX3 for the chip set. If you have not already done so, you must also enable I/O APIC on the same tab.

##QuickStart KVM Image
	The KVM image provides a raw disk image that can be used by many hypervisors. Configure machines that use this image with sufficient RAM. See Cloudera QuickStart VM for the VM size requirements.
	
#组件说明
##Flume
	Flume 从几乎所有来源收集数据并将这些数据聚合到永久性存储（如 HDFS）中。
	
##HBase
	Apache HBase 提供对大型数据集的随机、实时的读/写访问权限（需要 HDFS 和 ZooKeeper）。
	
##HDFS
	Apache Hadoop 分布式文件系统 (HDFS) 是 Hadoop 应用程序使用的主要存储系统。HDFS 创建多个数据块副本并将它们分布在整个群集的计算主机上，以启用可靠且极其快速的计算功能。
	
##Hive
	Hive 是一种数据仓库系统，提供名为 HiveQL 的 SQL 类语言。
		
##Hue
	Hue 是与包括 Apache Hadoop 的 Cloudera Distribution 一起配合使用的图形用户界面（需要 HDFS、MapReduce 和 Hive）。
	
##Impala
	Impala 为存储在 HDFS 和 HBase 中的数据提供了一个实时 SQL 查询接口。Impala 需要 Hive 服务，并与 Hue 共享 Hive Metastore。
	
##Key-Value Store Indexer
	键/值 Store Indexer 侦听 HBase 中所含表内的数据变化，并使用 Solr 为其创建索引。
	
##MapReduce
	Apache Hadoop MapReduce 支持对整个群集中的大型数据集进行分布式计算（需要 HDFS）。建议改用 YARN（包括 MapReduce 2）。包括 MapReduce 用于向后兼容。
	
##Oozie
	Oozie 是群集中管理数据处理作业的工作流协调服务。
	
##Solr
	Solr 是一个分布式服务，用于编制存储在 HDFS 中的数据的索引并搜索这些数据。
	
##Spark
	Apache Spark is an open source cluster computing system
	
##Sqoop
	Sqoop 是一个设计用于在 Apache Hadoop 和结构化数据存储（如关系数据库）之间高效地传输大批量数据的工具。Cloudera Manager 支持的版本为 Sqoop 2。
	
##Sqoop 1 Client
	Configuration and connector management for Sqoop 1.
	
##YARN (MR2 Included)
	Apache Hadoop MapReduce 2.0 (MRv2) 或 YARN 是支持 MapReduce 应用程序的数据计算框架（需要 HDFS）。
	
##ZooKeeper
	Apache ZooKeeper 是用于维护和同步配置数据的集中服务。	
