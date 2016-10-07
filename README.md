# ApiSpeechRecognition

##Préambule
ApiSpeechRecognition est une application python utilisant des API tel que PyAudio, SpeechRecognition, etc..
Le but est d'être __modifiable a souhait__! cette version est la version Api pour python.

##Installation:
    script linux (en root):
       pip install lsr

##Configuration:
    vous pouvez modifier les fichiers config de l'api yml pour votre application avec:
        https://raw.githubusercontent.com/EkiVox/SourceSpeechRecognition/master/configurator.py
##Utilisation:
    mettez dans votre application:
        import lsr

    pour lancer l'écoute:
        variablequetuveux = lsr.recognition.listening
    pour verifier s'il y a correspondance avec votre fichier config.yml et dans ce cas faire la commande + faire parler l'ordi:
        lsr.recognition.match(variableprécédente, "ton fichier de config", "ta langue")

##Exemple:

    import lsr
    phrase = lsr.recognition.listening
    print("selon moi tu as dit " + phrase + "!")
    lsr.recognition.match(phrase, "config.yml", "fr")

##Erreurs possibles:
    Failed loading libsmpeg-0.4.so.0:
        solution: sudo apt-get install libsmep-dev
