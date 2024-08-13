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

OPENAI Key: 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

ps -ef|grep LLMOps(가상환경 이름)

PS C:\Windows\system32> Get-ExecutionPolicy
Restricted
PS C:\Windows\system32> Set-ExecutionPolicy RemoteSigned

pip install -r requirements.txt
pip install numpy==1.26.4

=================================================
curl http://localhost:11434/v1/chat/completions \
-H "Content-Type: application/json" \
-d '{
"model": "llama3.1",
"messages": [
{
"role": "system",
"content": "You are a helpful assistant."
},
{
"role": "user",
"content": "머신러닝에 대해서 설명해줘."
}
]
}'





from openai import OpenAI

client = OpenAI(
base_url = 'http://localhost:11434/v1',
api_key='ollama', # required, but unused
)

response = client.chat.completions.create(
model="llama3.1",
messages=[
{"role": "system", "content": "You are a helpful assistant."},
{"role": "user", "content": "Who won the world series in 2020?"},
{"role": "assistant", "content": "The LA Dodgers won in 2020."},
{"role": "user", "content": "Where was it played?"}
]
)
print(response.choices[0].message.content)
==========================================================================

from openai import OpenAI

client = OpenAI(
base_url = 'https://1d44-14-35-173-251.ngrok-free.app/v1',
api_key='ollama', # required, but unused
)

response = client.chat.completions.create(
model="for_vllm",
messages=[
{"role": "system", "content": "You are a helpful assistant."},
{"role": "user", "content": "Who won the world series in 2020?"},
{"role": "assistant", "content": "The LA Dodgers won in 2020."},
{"role": "user", "content": "오늘 날씨 어때?"}
]
)
print(response.choices[0].message.content)