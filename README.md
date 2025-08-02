# roll_dice_gui
file1_path = input("Enter path of first file: ")
file2_path = input("Enter path of second file: ")

with open(file1_path, 'r') as file1:
    text1 = file1.read()

with open(file2_path, 'r') as file2:
    text2 = file2.read()

total_char = max(len(text1), len(text2))
same_char=0

for i in range(total_char):
    if i < len(text1) and i < len(text2):
        if text1[i] == text2[i]:
            same_char+= 1

if total_char > 0:
    similarity = (same_char / total_char) * 100
else:
    similarity = 0

print(f"The files are {similarity}% similar based on characters.")
