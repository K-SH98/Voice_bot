# 음성 기반 AI 상담 챗봇
이 프로젝트는 OpenAI의 GPT-4o 모델을 활용하여 사용자의 고민을 듣고 공감하며 조언해주는 음성 기반의 AI 상담 챗봇입니다. 사용자의 말을 실시간으로 인식하고, 자연스러운 음성으로 답변하며, 이전 대화 내용을 기억하여 맥락에 맞는 상담을 제공합니다.

---

✨ 주요 기능
음성 인식 (Speech-to-Text): SpeechRecognition 라이브러리를 사용해 사용자의 음성을 텍스트로 변환합니다.

AI 상담가 (GPT-4o): OpenAI의 gpt-4o 모델을 통해 사용자의 고민에 공감하고, 해결책을 찾도록 유도하는 질문과 조언을 생성합니다.

음성 합성 (Text-to-Speech): pyttsx3 라이브러리를 사용해 챗봇의 답변을 자연스러운 음성으로 출력합니다.

대화 기억: 이전 대화 내용을 chat_history에 저장하여, 사용자가 이전에 했던 말을 기억하고 맥락에 맞는 답변을 제공합니다.

---

🛠️ 사용 기술
Python: 주 개발 언어

OpenAI API: GPT-4o 모델 활용

Libraries:

openai: OpenAI API 사용을 위한 라이브러리

speechrecognition: 음성 인식을 위한 라이브러리

pyttsx3: 텍스트-음성 변환(TTS)을 위한 라이브러리

python-dotenv: 환경 변수(API 키) 관리를 위한 라이브러리

---

### ⚙️ 설치 및 실행 방법

1. 사전 준비
- Python 3.7 이상 버전이 설치되어 있어야 합니다.

- 음성 입력을 위한 마이크가 필요합니다.

2. 라이브러리 설치
- 프로젝트에 필요한 라이브러리를 설치합니다.

(Bash) pip install openai speechrecognition pyttsx3 python-dotenv

3. OpenAI API 키 설정
- 프로젝트 루트 디렉토리에 .env 파일을 생성하고, 아래와 같이 자신의 OpenAI API 키를 입력합니다.
-> OPENAI_API_KEY="여기에_자신의_API_키를_입력하세요"
  
4. 실행
- Python 스크립트 또는 Jupyter Notebook에서 run_voice_chatbot() 함수를 실행합니다.

(Python) run_voice_chatbot()
프로그램이 실행되면 "🎙️ 대화 시작..." 메시지가 나타납니다. 마이크에 대고 말을 시작하세요. 대화를 종료하고 싶을 때는 "그만"이라고 말하면 됩니다.

📄 코드 구조
listen_chatbot(): 사용자의 음성을 마이크로 입력받아 텍스트로 변환하는 함수입니다.

read_chatbot(): 챗봇의 텍스트 응답을 음성으로 변환하여 출력하는 함수입니다.

run_voice_chatbot(): 전체적인 대화 흐름을 관리하는 메인 함수입니다. 사용자의 입력을 받고, OpenAI API를 호출하여 답변을 생성한 뒤, 음성으로 출력하는 과정을 반복합니다. 또한, 대화의 맥락을 유지하기 위해 이전 대화 기록을 관리합니다.
