the script:

'''
echo "# lot_of_commits" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:YOUR REPO
git push -u origin main


'''

'''
HOW TO FARM:
'''

import time
import subprocess

com1 = 'cd /home/dev/repopush; git add .'
com2 = 'cd /home/dev/repopush; git commit -m "another yet commit"'
com3 = 'cd /home/dev/repopush; git push -u origin main'

for i in range(10000):
    with open('/home/dev/repopush/some_file.txt', 'w') as f:
        f.write('meow')
        f.write(str(i))
        f.write('\n')

    
    time.sleep(2)
    print('sleep 5 sec')

    try:
        result1 = subprocess.check_output(com1, shell=True)
        print(result1) 
    except:
        print('err1')

    try:
        result2 = subprocess.check_output(com2, shell=True)
        print(result2) 
    except:

        print('err2')

    try:
        result3 = subprocess.check_output(com3, shell=True)
        print(result3) 
    except:
        print('err3')
