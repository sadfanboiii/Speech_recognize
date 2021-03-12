import speech_recognition as sr
import pyttsx3 as tts



r = sr.Recognizer()
engine = tts.init()
engine.setProperty('rate', 200)


def speak(text):
	engine.say(text)
	engine.runAndWait()


def getText():
	with sr.Microphone() as source:
		try:
			print("Powiedz coś...")
			audio = r.listen(source)
			text = r.recognize_google(audio, language='pl-PL')
			if text != "":
				return text
			return 0
		except:
			return 0


while True:
	txt = getText()
	if not txt == 0:
		print(txt)
		speak(txt)
		break
	else:
		print("Nic nie usłyszałem...")
		continue
