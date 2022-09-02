# suricata_rule

snort(suricata) rule 파일을 제작하여 특정 사이트 트래픽을 탐지하여라.
```
suricata -s test.rules -i eth0<br>
tail -f /var/log/suricata/fast.log
```
### 상세
- test.rules 파일에 20개의 사이트를 탐지하는 룰을 만든다.
- 이후 fast.log를 확인하면서 20개의 사이트가 제대로 탐지되는지 확인을 해 본다(rules 파일내의 모든 sid가 fast.log파일에 로그로 남아야 한다).
- 평문 통신(HTTP)이 이루어 지는 사이트 뿐만 아니라 TLS 통신(HTTPS)을 하는 사이트에 대한 탐지를 구현해 본다.

![fast.log](https://github.com/seungwook0417/suricata_rule/blob/main/resource/01.png)