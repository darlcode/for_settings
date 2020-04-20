# terminal_commands
 Description of various commands for terminal

1. How to check Ubuntu version in terminal<br>
*(우분투 버전 확인 명령어)*<br>
`$ lsb_release -a`

2. How to check linux disk free spaces in terminal <br>
*(디스크의 남은 용량 확인 명령어)*<br>
df 명령을 사용하면 linux 시스템에 마운트된 디스크 사용량을 확인할 수 있음<br>
**사용형식: df [OPTION]... [FILE]...**<br>
`$ df --help` 참고<br>
`$ df`
![image](https://user-images.githubusercontent.com/61573968/79690823-72727e00-8297-11ea-96f3-7d0c1ae687b1.png)
`$ df -h` # -h: human readable option을 주면 MB,GB단위로 표기해줌
![image](https://user-images.githubusercontent.com/61573968/79690840-95049700-8297-11ea-9bf2-9c95ef62ba70.png)

3. How to check linux directory usage in terminal <br>
*(디렉토리의 사용량 확인 명령어)*<br>
**사용형식: du [OPTION]... [FILE]...**<br>
`$ du --help`참고<br>
`$ du`<br>
![image](https://user-images.githubusercontent.com/61573968/79691131-d0539580-8298-11ea-9278-30c1cb526056.png)<br>
`$ du -h`<br>
![image](https://user-images.githubusercontent.com/61573968/79691224-33ddc300-8299-11ea-89e0-28d814656691.png)<br>
`$ du -h <확인하고픈 디렉토리>` # 확인하고픈 특정 디렉토리 지정 가능<br>
![image](https://user-images.githubusercontent.com/61573968/79691406-3db3f600-829a-11ea-8642-ae70017ee861.png)<br><br>
`$ du -sh <확인하고픈 디렉토리>` # 확인하고픈 디렉토리의 요약<br>
![image](https://user-images.githubusercontent.com/61573968/79691444-81a6fb00-829a-11ea-9fda-c87be115a793.png)



