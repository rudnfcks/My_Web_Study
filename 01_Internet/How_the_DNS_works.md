# DNS가 작동하는 원리

**DNS (Domain Name System) :**

컴퓨터가 통신하기 위해서는 IP 라는 숫자로 이루어진 주소를 사용하는데, 192.168.0.1 과 같은 숫자 IP 주소를 'www.naver.com' 과 같이 사람이 읽을 수 있는 이름으로 변환하여 사람이 사용하기 편하게 하기 위한 시스템

# ✏ DNS 작동 원리

1. 웹 브라우저에서 사용자가 문자로 이루어진 'www.naver.com' 주소를 입력한다.

   → **Local DNS**에 해당 문자주소가 존재하는지 확인한다.

   → 없다면 다른 **DNS 서버의 정보**를 받는다.

2. Root DNS 서버에 'www.naver.com' 주소에 대해 물어본다.

   → 'com 도메인'을 관리하는 TLD (Top-Level Domain) 이름 서버 정보를 받는다.

3. TLD 서버에 'www.naver.com' 주소에 대해 물어본다.

   → TLD 서버에서 'naver.com' 주소를 관리하는 DNS 서버 정보를 받는다.

4. 'naver.com' 주소를 관리하는 DNS서버에 'www.naver.com'에 대한 IP 주소를 물어본다.

   → Local DNS에게 'www.naver.com'에 대한 숫자로 이루어진 IP를 전달한다.

5. Local DNS가 'www.naver.com'에 대한 IP 주소를 캐싱하고 IP 주소 정보를 전달한다.

### ❗이로써 주소창에 문자 주소를 넣으면 해당 주소의 IP를 통해 서버와 통신한다.
