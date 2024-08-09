학습사이트주소
https://samsung-ai.elice.io/courses/367078/boards/6722/articles/50098

vscode 설정
Host elice_instance
  HostName 14.35.173.14
  Port 59711
  User elicer
  IdentityFile C:\Users\User\elice-cloud-ondemand-ea436aae-83f1-4507-8477-eeb2c7cbb238.pem

가상환경
python -m venv vrupin
source ./vrupin/bin/activate
빠져나오기는 deactivate

필요한 패키지 설치
pip install -r ../requirements.txt

import huggingface_hub
# huggingface_hub.login("YOUR_API_KEY")
huggingface_hub.login("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")

weight and bias
wandb.ai: 1c65a95d06626786e604422c8a5d26ad37b3c431
1c65a95d06626786e604422c8a5d26ad37b3c431


ps -ef|grep LLMOps(가상환경 이름)