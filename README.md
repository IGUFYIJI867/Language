from googletrans import Translator
p=int(input("Want in hindi ? say 1 for yes and 2 for no : "))
translator = Translator()
# translate a spanish text to english text (by default)
try:
    if p==2:
        print("Welcome to Language Translator")
        for i in range(20):
            a=input("\nEnter the destination language : ")
            b=input("Enter text : ")
            translation = translator.translate(b,dest=a)
            print(f"{translation.text}")
            q=input("Want to Continue ?[Y/N]")
    elif p==1:
        print("भाषा अनुवादक मे स्वागत है")
        for i in range(20):
            a=input("\nगन्तव्य भाषा दर्ज करें : ")
            b=input("पाठ दर्ज करें : ")
            translation = translator.translate(b,dest=a)
            print(f"{translation.text}")
            q=input("दुबरा इस्तेमाल करना चाहते है?[Y/N]")
except Exception as e:
        print(f"{e}")
