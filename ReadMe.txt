v1.0 HdMod has been developed by ZarfaZ (zarfaz@mail.ru) in May 2019. 
This is set of HD textures for game Diggles: The Myth of Fenris. 
If you spot any bug except known ones (descibed in the bottom of this file) please write me an e-mail with screenshot and detailed description what is wrong and how did you manage to achieve such effect.

-------ENGLISH-----------------
Implementing any version:
1) Implement Full version
2) Copy and replace files from your version
3) Full version has RU by default

Implementing Full version:
1) Backup existing folders:
	\Data\Texture
	\Data\Ground
2) Implement HD Ground: Replace full folder \Data\Ground
3) Implement HD textures has 2 equal ways:
	Way I. Copy and replace files with same paths:
		\Data\Texture\m032
		\Data\Texture\m064
		\Data\Texture\m128
		\Data\Texture\m256
		\Data\Texture\Misc //WARNING: this folder does not contain full set of textures, so replace overlapping file and do not delete odd ones
		\Data\Texture\ClassIcons
	Way II. Idea is to collect m032-m256 textures in a single folder \m256.
		a) Delete content of folders:
			\Data\Texture\m032
			\Data\Texture\m064
			\Data\Texture\m128
			\Data\Texture\m256
		b) Copy files
			FROM \FullVersion\Textures\m032 TO \Data\Texture\m256
			FROM \FullVersion\Textures\m064 TO \Data\Texture\m256
			FROM \FullVersion\Textures\m128 TO \Data\Texture\m256
			FROM \FullVersion\Textures\m256 TO \Data\Texture\m256
		c) Copy and replace files with same path:
			\Data\Texture\Misc
			\Data\Texture\ClassIcons

Known bugs:
1) Engiene does not recognize ground transition masks with resolution higher that 64x64 pixels for files like "\Data\Ground\Msk_AAAB01.tga". 
For different type of ground joints this result into hard visualisation without smooth transition. 
In a normal way 2 different ground should be visualized on the same polygon with applied transition mask to smooth joint, but in case of high res ground it works only for limited block (for area eual to 64x64).
So there is no smooth transition between 2 different types of ground, it looks like all world consist of sharp square blocks.

			