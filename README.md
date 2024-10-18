# Saving data program

# -------------------------
# Subprograms
# -------------------------
def load(filename):
    file = open(filename, "r")
    user = file.read()
    file.close()
    user = user.strip()
    return user


def save(user, filename):
    file = open(filename, "w")
    user = user + "\n"
    file.write(user)
    file.close()


# -------------------------
# Main program
# -------------------------

blank = load('datafile.txt')
if blank == '':
  print("Hello, I don't believe we have met.")
  name = input('What is your name? ')
  save(name,'datafile.txt')
  print('nice to meet you', name)
else:
  print("It's good to see you again,", blank)
