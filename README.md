# PRODIGY_CS_01
#Caesar Cipher Algorithm

alphabet=['a','b','c','d','e','f','g','h','i','j','k','l','m','n',
          'o','p','q','r','s','t','u','v','w','x','y','z']

def encryption(plain_text,shift_key):
    cipher_text=""
    for char in plain_text:
        position=alphabet.index(char)
        new_position=(position+shift_key)%26
        cipher_text+=alphabet[new_position]
    print(f"Here's is the text after encryption: {cipher_text}")
def decryption(cipher_text,shift_key):
    plain_text=""
    for char in cipher_text:
        position=alphabet.index(char)
        new_position=(position-shift_key)%26
        plain_text+=alphabet[new_position]
    print(f"Here's is the text after Decryption :{plain_text}")
    
wanna_end=False
while not wanna_end:
    method=input("Type 'encrypt' for Encryption, type 'decrypt' for decryption:\n")
    text=input("enter the Text:\n")
    shift=int(input("Enter the shift key :\n"))
    if method=="encrypt":
        encryption(plain_text=text,shift_key=shift)
    elif method=="decrypt":
        decryption(text,shift)
    play_again=input("Type yes for continue,Type no to exit.\n")
    if play_again=='no':
        wanna_end=True
        print("Have a nice day! byee..")

