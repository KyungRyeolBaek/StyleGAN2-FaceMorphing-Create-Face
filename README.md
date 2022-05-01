# StyleGAN2-FaceMorphing-Create-Face
StyleGAN2와 Face-Morphing을 이용한 가상 얼굴 생성 프로젝트입니다.

기업 협업 프로젝트 입니다.

스타일봇 기업의 요구 사항에 맞춰 프로젝트를 진행하였습니다.

요구사항 : 동양인이 선호하는 가상의 귀여운 얼굴형 이미지 생성 요청.

생각보다 가상 이미지가 잘 나와 신기했던 프로젝트이었습니다.

영상 : https://youtu.be/pZDXPQz2rXM
#
진행 순서 : 
1. 학습을 위한 데이터를 DownAlbum을 이용하여 수집하였습니다. ( 특정한 원하는 이미지를 얻고 싶을 때 사용하셔요 !! 추천드립니다. )
  - DownAlbum 사용 방법 : https://www.notion.so/Down-Album-a513efc8bdb3443698e52dc4895357d5
  - ![image](https://user-images.githubusercontent.com/40240766/166129141-b92ef772-8c34-4ef0-ae2a-56f6a2d4fd6f.png)
  - FaceBook이나 Instagram에 있는 원하는 연예인 이미지 사진들을 모을 수 있습니다.
#
2. 수집한 데이터를 학습에 좋은 이미지로 바꾸기 위해 얼굴 형태와 얼굴의 위치를 중앙으로 모았습니다.
  - 위의 작업을 진행하기 위해 Face Morphing을 사용하여 얼굴 선을 찾아내 이미지를 재편집하여 사용하였습니다.
  - FaceMorphing 사용 방법 : https://airy-attempt-22a.notion.site/a939b61381c24388a1abb85038805f64
  - ![image](https://user-images.githubusercontent.com/40240766/166129065-e051e418-25dc-4d82-8f71-daeea932c618.png)
  - 수집했던 이미지를 열어 그 이미지에 얼굴 형태의 부분이 있으면 그 부분을 잘라내고 저장까지 해줍니다. 
  - ( 수많은 이미지를 어떻게 잘라낼까 걱정했는데 다행이 이런 코드를 짜주신 분이 !! )
#
3. 현존하지 않는 이미지를 생성 해야 했기에 이미지 생성 모델인 GAN 중 StyleGAN2를 이용했습니다.
  - GAN은 Generative Adversarial Network의 줄임말으로써 서로 경쟁을 하며 학습하는 네트워크 중 하나이다.
  - GAN에는 다양한 파생 네트워크들이 많은데 그 중 하나가 StyleGAN이다.
  - GAN ~ StyleGAN2 설명 : https://www.notion.so/GAN-StyleGAN2-28db3fa1a6dd4ec5b072488beaec9072
  - ![image](https://user-images.githubusercontent.com/40240766/166129335-2f6bac07-67e6-4353-bdd6-ba89c0307ebe.png)
  - StyleGAN2를 잘 표현해준 이미지중 하나이다 ! 
  - 다른 두 이미지의 형태를 따와 새로운 이미지를 생성한다. 
  - SorceA에서는 전체적인 큰 틀(얼굴형, 머리 모양 등)을 따오고, SorceB에서는 세부적인 요소(눈매, 코, 치아, 머리카락 질감)들을 따온다.
#
다음과 같이 진행 하면 새로운 형태의 가상 이미지를 생성 해 낼 수 있습니다.

연예인 츄(Chu)와 박보영의 이미지를 사용하여 새로운 가상 이미지들을 생성 해 냈습니다.

<img src="https://user-images.githubusercontent.com/40240766/141887474-e2cafdd6-e1fb-4a3d-8c71-5b1dbfba2316.png" width="400" height="400"/> <img src="https://user-images.githubusercontent.com/40240766/141887480-49190cdb-2ade-477a-94bf-111ef59a255f.png" width="400" height="400"/>
<img src="https://user-images.githubusercontent.com/40240766/141887481-2b81cfe2-2a1f-4132-820f-9e5a5496e33d.png" width="400" height="400"/>
<img src="https://user-images.githubusercontent.com/40240766/141887483-1a644e23-e6f8-4403-8001-0d544115cfa6.png" width="400" height="400"/>
<img src="https://user-images.githubusercontent.com/40240766/141887487-c704d81f-fa41-49f7-adbf-1ce8be730149.png" width="400" height="400"/>
<img src="https://user-images.githubusercontent.com/40240766/141888550-55f059df-2d31-4447-87d9-ba9f634d874d.png" width="400" height="400"/>
<img src="https://user-images.githubusercontent.com/40240766/141889915-481ff943-9458-4ebf-b1c2-2fe86f5931c0.png" width="400" height="400"/>
<img src="https://user-images.githubusercontent.com/40240766/141889921-f82dbe68-7c47-41f5-ad4a-0ee7766269bf.png" width="400" height="400"/>

이미지의 얼굴 부분은 별로 큰 위화감이 들지 않지만 손부분이나 장신구 부분을 자세히 보면 Fake 이미지라는 것을 확인 할 수 있다.

기업 협업으로 두명이지만 팀을 이뤄서 했던 프로젝트여서 서로 소통하며 코드를 수정하는 경험이 색달랐다.

문자로 서로의 소통이 잘 되지 않을 땐 화상 회의를 통해 얘기를 하니 금방 풀리는 경우가 있었다.

결과가 나쁘진 않았지만, 조금 더 다듬었으면 좋은 결과를 내지 않았을까 싶은 생각이 드는 프로젝트였다.

감사합니다.
