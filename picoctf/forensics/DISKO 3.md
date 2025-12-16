i did mmls but it gave no output so i searched what that meant it meant that the image had so partitions, i did fsstat and got an output which meant that the file was correct,
```
akalra@akalra:~/Desktop/picoctf/forencis$ fsstat disko-3.dd
FILE SYSTEM INFORMATION
--------------------------------------------
File System Type: FAT32

OEM Name: mkfs.fat
Volume ID: 0x49838d0b
Volume Label (Boot Sector): NO NAME    
Volume Label (Root Directory):
File System Type Label: FAT32   
Next Free Sector (FS Info): 36434
Free Sector Count (FS Info): 1375

Sectors before file system: 0

File System Layout (in sectors)
Total Range: 0 - 204799
* Reserved: 0 - 31
** Boot Sector: 0
** FS Info Sector: 1
** Backup Boot Sector: 6
* FAT 0: 32 - 1607
* FAT 1: 1608 - 3183
* Data Area: 3184 - 204799
** Cluster Area: 3184 - 204799
*** Root Directory: 3184 - 3184

METADATA INFORMATION
--------------------------------------------
Range: 2 - 3225862
Root Directory: 2

CONTENT INFORMATION
--------------------------------------------
Sector Size: 512
Cluster Size: 512
Total Cluster Range: 2 - 201617

FAT CONTENTS (in sectors)
--------------------------------------------
3184-3184 (1) -> EOF
3185-3185 (1) -> 35629
3186-3186 (1) -> EOF
3187-3187 (1) -> EOF
3188-3188 (1) -> EOF
3189-3189 (1) -> EOF
3190-3190 (1) -> EOF
3191-3191 (1) -> EOF
3192-3192 (1) -> 35627
3193-3193 (1) -> EOF
3194-3431 (238) -> EOF
3432-31597 (28166) -> EOF
31598-31668 (71) -> EOF
31669-31828 (160) -> EOF
31829-35208 (3380) -> EOF
35209-35473 (265) -> EOF
35474-35626 (153) -> EOF
35627-35627 (1) -> EOF
35628-35628 (1) -> EOF
35629-35629 (1) -> 35848
35630-35636 (7) -> EOF
35637-35673 (37) -> EOF
35674-35715 (42) -> EOF
35716-35716 (1) -> EOF
35717-35808 (92) -> EOF
35809-35847 (39) -> EOF
35848-35848 (1) -> 37889
35849-36433 (585) -> EOF
36434-36434 (1) -> EOF
37810-37810 (1) -> EOF
37811-37858 (48) -> EOF
37859-37859 (1) -> 37884
37860-37866 (7) -> EOF
37867-37875 (9) -> EOF
37876-37877 (2) -> EOF
37878-37879 (2) -> EOF
37880-37883 (4) -> EOF
37884-37884 (1) -> EOF
37885-37887 (3) -> EOF
37888-37888 (1) -> EOF
37889-37889 (1) -> 37950
37890-37895 (6) -> EOF
37896-37936 (41) -> EOF
37937-37937 (1) -> EOF
37938-37942 (5) -> EOF
37943-37949 (7) -> EOF
37950-37950 (1) -> 39157
37951-37965 (15) -> EOF
37966-37966 (1) -> EOF
37967-37967 (1) -> EOF
37968-37968 (1) -> 38283
37969-38157 (189) -> EOF
38158-38170 (13) -> EOF
38171-38281 (111) -> EOF
38282-38282 (1) -> EOF
38283-38283 (1) -> 38962
38284-38284 (1) -> EOF
38285-38287 (3) -> EOF
38288-38648 (361) -> EOF
38649-38873 (225) -> EOF
38874-38945 (72) -> EOF
38946-38961 (16) -> EOF
38962-38962 (1) -> EOF
38963-38964 (2) -> EOF
38965-38971 (7) -> EOF
38972-38985 (14) -> EOF
38986-39156 (171) -> EOF
39157-39157 (1) -> 40882
39158-39665 (508) -> EOF
39666-40236 (571) -> EOF
40237-40237 (1) -> EOF
40238-40802 (565) -> EOF
40803-40817 (15) -> EOF
40818-40818 (1) -> EOF
40819-40881 (63) -> EOF
40882-40882 (1) -> EOF
40883-40919 (37) -> EOF
40920-41235 (316) -> EOF
41236-41236 (1) -> EOF
41237-41237 (1) -> EOF
41238-41238 (1) -> EOF
41239-41239 (1) -> 50198
41240-50197 (8958) -> EOF
50198-50198 (1) -> 68162
50199-59184 (8986) -> EOF
59185-68161 (8977) -> EOF
68162-68162 (1) -> 85946
68163-77136 (8974) -> EOF
77137-85945 (8809) -> EOF
85946-85946 (1) -> 204795
85947-200634 (114688) -> EOF
200635-204794 (4160) -> EOF
204795-204799 (5) -> EOF
```
then i did fls to find the file which contained the flag and i got it and then i extracted it using the icat 
```
akalra@akalra:~/Desktop/picoctf/forencis$ fls -r disko-3.dd
d/d 4:	log
+ d/d 22:	private
+ d/d 24:	sysstat
+ d/d 26:	stunnel4
++ r/r 70:	stunnel.log
+ d/d 28:	mysql
+ d/d 30:	inetsim
++ d/d 102:	report
+ d/d 32:	installer
++ d/d 134:	cdebconf
+++ r/r 150:	questions.dat
+++ r/r 152:	templates.dat
++ r/r 136:	Xorg.0.log
++ r/r 138:	partman
++ r/r 140:	syslog
++ r/r 143:	hardware-summary
++ r/r 145:	status
++ r/r 519091:	lsb-release
+ r/r 519123:	vmware-vmsvc-root.2.log
+ r/r 519125:	kern.log.4.gz
+ r/r 519127:	Xorg.0.log
+ r/r 519130:	vmware-network.4.log
+ r/r 519132:	boot.log
+ r/r 519134:	syslog.3.gz
+ r/r 519137:	vmware-vmtoolsd-root.log
+ r/r 522627:	daemon.log
+ r/r 522628:	flag.gz
+ r/r * 522629:	_ESSAGES
+ r/r 522632:	alternatives.log.2.gz
+ r/r 522634:	debug
+ d/d 522636:	lightdm
++ r/r 554806:	lightdm.log
++ r/r 554809:	lightdm.log.old
++ r/r 554811:	x-0.log
++ r/r 554813:	x-0.log.old
++ r/r 554816:	seat0-greeter.log
++ r/r 555203:	seat0-greeter.log.old
+ r/r 522639:	vmware-network.6.log
+ r/r 522642:	alternatives.log
+ r/r 555285:	vmware-vmsvc-root.1.log
+ r/r 555288:	Xorg.0.log.old
+ r/r 555291:	vmware-network.8.log
+ r/r 555294:	vmware-vmsvc-root.log
+ r/r 555297:	vmware-vmsvc-root.3.log
+ r/r 556259:	boot.log.6
+ r/r 556262:	vmware-network.5.log
+ r/r 556265:	macchanger.log.4.gz
+ d/d 556267:	apt
++ r/r 556550:	eipp.log.xz
++ r/r 556552:	history.log
++ r/r 556554:	term.log.2.gz
++ r/r 556557:	history.log.5.gz
++ r/r 556559:	term.log
++ r/r 556561:	term.log.1.gz
++ r/r 561588:	history.log.1.gz
++ r/r 561591:	history.log.2.gz
++ r/r 561593:	term.log.5.gz
++ r/r 561595:	term.log.4.gz
++ r/r 561598:	history.log.4.gz
++ r/r 561600:	term.log.3.gz
++ r/r 572451:	history.log.3.gz
+ r/r 556269:	dpkg.log.1
+ r/r 556271:	boot.log.5
+ r/r 556273:	wtmp
+ r/r 575571:	dpkg.log.5.gz
+ r/r 575573:	lastlog
+ r/r 575576:	vmware-network.3.log
+ r/r 575578:	syslog.4.gz
+ r/r 575580:	boot.log.1
+ r/r 575583:	vmware-network.2.log
+ r/r 575585:	faillog
+ r/r 603171:	kern.log.3.gz
+ r/r 603173:	dpkg.log.4.gz
+ r/r 603176:	vmware-network.1.log
+ r/r 603179:	vmware-network.7.log
+ d/d 603181:	journal
++ d/d 608872:	480afdbb61874a758c0b53617cfc8e8f
+++ r/r 608892:	system@7a442d5ca4df4e0f9507094c9269ca6a-0000000000005a8a-0006054ede6dfcb2.journal
+++ r/r 752228:	system@d902d27452664082ae8a9ac82cb69ba1-0000000000004b19-0006054ecec0fb53.journal
+++ r/r 752236:	system@b0aa03528b9c43dc896b9ab01ba4c893-00000000000042ae-0006054ec01755dc.journal
+++ r/r 1039652:	system@fe4e86893ffe4006869e03921f0c0c32-00000000000052d8-0006054edbce9160.journal
+++ r/r 1039660:	system@54b9f53d65d44041abdf784998995b81-000000000000624c-0006054ef1ae82cf.journal
+++ r/r 1324196:	system@185d88d5eb13416d80fa5cb1c5faf4d0-000000000000a97e-00062a2783e88318.journal
+++ r/r 1324199:	user-1000.journal
+++ r/r 1324207:	system@185d88d5eb13416d80fa5cb1c5faf4d0-000000000001feae-00062ba433aaa6e0.journal
+++ r/r 3225783:	system@d902d27452664082ae8a9ac82cb69ba1-00000000000050fb-0006054ed43fd222.journal
+++ r/r 3225791:	system@24d583de9c1a4252813ff1f373a8814d-0000000000006989-00060561dfa7e3c8.journal
+++ r/r 3225799:	system@185d88d5eb13416d80fa5cb1c5faf4d0-00000000000070c7-0006224d2862127d.journal
+++ r/r 3225807:	user-1000@d902d27452664082ae8a9ac82cb69ba1-00000000000050fa-0006054ed43ef163.journal
+++ r/r 3225815:	user-1000@94309907b19d4653afc79e24b6eec039-00000000000005b4-0005e76be8304b42.journal
+++ r/r 3225820:	system@0006054e6fd33237-813b83aec6062020.journal~
+++ r/r 3225828:	user-1000@185d88d5eb13416d80fa5cb1c5faf4d0-000000000002374d-00062eff8e6c0038.journal
+++ r/r 3225836:	system@fe4e86893ffe4006869e03921f0c0c32-00000000000058b3-0006054edc51935b.journal
+++ r/r 3225844:	user-1000@fe4e86893ffe4006869e03921f0c0c32-00000000000058b2-0006054edc4fe35c.journal
+++ r/r 3225849:	user-1000@0006054e70c65fc3-7af43b1c79f1269a.journal~
+++ r/r 3225857:	system@7a442d5ca4df4e0f9507094c9269ca6a-000000000000605c-0006054ee0dded41.journal
+ r/r 603184:	vmware-network.log
+ r/r 603186:	dpkg.log.2.gz
v/v 3225859:	$MBR
v/v 3225860:	$FAT1
v/v 3225861:	$FAT2
V/V 3225862:	$OrphanFiles
akalra@akalra:~/Desktop/picoctf/forencis$ icat disko-3.dd 522628 > flag.gz
akalra@akalra:~/Desktop/picoctf/forencis$ ls
disk.img.gz  disko-3.dd  flag.gz
akalra@akalra:~/Desktop/picoctf/forencis$ file flag.gz
flag.gz: gzip compressed data, was "flag", last modified: Thu Jul 17 15:06:53 2025, from Unix, original size modulo 2^32 53
akalra@akalra:~/Desktop/picoctf/forencis$ gzip -d flag.gz
akalra@akalra:~/Desktop/picoctf/forencis$ ls
disk.img.gz  disko-3.dd  flag
akalra@akalra:~/Desktop/picoctf/forencis$ cat flag
Here is your flag
picoCTF{n3v3r_z1p_2_h1d3_26d4f233}

```
**FLAG =  picoCTF{n3v3r_z1p_2_h1d3_26d4f233}**
