# QRRR! 

At the start of the challenge we get a file `QRRR!.gif`

![{DF858E03-2CE6-48A4-8887-A05E00E464A9}](https://github.com/user-attachments/assets/8dee5761-6b15-433b-a1e5-9697c9518a37)

I will upload the file to the first page from google [QrREADER](https://scanqr.org/)
![{DCCF79CC-2DF3-450E-89FE-0C441B979194}](https://github.com/user-attachments/assets/5914d31a-c23c-4faa-a746-fda674e33754)

Well, and we have a flag!

![{C875F0B2-A149-4A8B-B02E-0C0E19429B09}](https://github.com/user-attachments/assets/a768b192-7a5d-4881-9a00-2b1103c4e56a)


Or we don't have :)

![{58CE754A-1DAD-4BFD-989C-FFB803A31139}](https://github.com/user-attachments/assets/9a6b49b7-6bb0-49ec-a721-a39a67ada1ce)

I realized that we need to approach this challenge a little differently and split our gif into separate files.
I found a site [ezgif](https://ezgif.com/split/) that allows for this

![{EA367C09-CF49-44D8-BD97-B82C819E3852}](https://github.com/user-attachments/assets/5c5f0b54-8c5c-42dc-9cb9-10fdb2894f82)

I received 62 files.
I read them all with the `zbarimg` tool.
Here is the result

![{C37AAFB2-2E0F-4155-8BFA-4F33AA68505A}](https://github.com/user-attachments/assets/54251194-a25a-47e5-849b-17bfe95818a5)

```
zbarimg frame_* > raw
cat raw| cut -d: -f2 > decoded_qrs.txt
sort decoded_qrs.txt | uniq -c | sort -nr
```

I thought it was all about a single string that is a uniquifier, but unfortunately I was wrong. There are several unique strings
![{EA057DA4-0A52-4FB8-B3F6-B70D752BA0BD}](https://github.com/user-attachments/assets/598795c5-5743-48e4-9bbc-f87b4273b767)

When I “flipped the signs” one text looked like the solution and it turned out to be a hit

![375770445-22323d58-877a-48bc-b9b1-7362784c24bb](https://github.com/user-attachments/assets/3bc43e85-5586-4689-9842-a69008eec24c)

![{0903AB2C-8A52-4655-893D-DD2E2984C3CD}](https://github.com/user-attachments/assets/80eacccd-42cb-4106-a47d-92c542412dc9)
