# Week 16 - Electronic Music DIY

# Easy 
## Question: Read the music sheet & Display
There are some sample sheet & music in sample/... :rotating_light:DO NOT:rotating_light: change them. 

1. Read both ***duration.txt*** and ***tone.txt*** files under same directory. 
2. Apply you learned so far, do some string handling to them.
3. Print all data like example below.

Do it with any method you want, or just check method in [System.IO.File](https://docs.microsoft.com/en-us/dotnet/api/system.io.file?view=net-5.0).

**Hint:** 

1. [String.Replace Method](https://docs.microsoft.com/en-us/dotnet/api/system.string.replace?view=net-5.0)
2. [String.Split Method](https://docs.microsoft.com/en-us/dotnet/api/system.string.split?view=net-5.0)

#### Example1:
#### Example2:
# Medium 
## Question: Use try-catch/throw let Wav function in MakeMusic.cs more robust.

Example usage of Wav function

```C#
static void Main(string[] args)
{
    MakeMusic.Wav(@"C:\Users\TA\workshop\week16\Sample\Dejavu\", "tone.txt", "duration.txt", "out0.wav");
    MakeMusic.Wav(@"C:\Users\TA\workshop\week16\Sample\Wily'sCastle\", "tone.txt", "duration.txt", "out1.wav", 1);
    MakeMusic.Wav(@"C:\Users\TA\workshop\week16\Sample\Megalovania\", "tone.txt", "duration.txt", "out2.wav", 2);
    MakeMusic.Wav(@"C:\Users\TA\workshop\week16\Sample\MagicForest\", "tone.txt", "duration.txt", "out3.wav", 3);
}
```

Here are some situation below that might make Wav function break.

1. File not found.
2. Path doesn't exist.
3. Duration and tone are not .txt format.
4. Output music file are not .wav format.

Use try-catch/throw to display different exception, then reminds user.

#### Example1:
```C#
// Case: File Not found
MakeMusic.Wav(@"C:\Users\TA\workshop\week16\Sample\Dejavu\", "TONE.txt", "DURATION.txt", "out0.wav");
```
#### Example2:
```C#
// Case: Path doesn;t exist
MakeMusic.Wav(@"C:\Users\TA\workshop\week9999\Sample\Wily'sCastle\", "tone.txt", "duration.txt", "out1.wav", 1);
```         
#### Example3:
```C#
// Case: Duration and tone are not .txt format.
MakeMusic.Wav(@"C:\Users\TA\workshop\week16\Sample\Megalovania\", "tone.dat", "duration.jpg", "out2.wav", 2);
```
#### Example4:
```C#
// Case: Output music file are not .wav format.
MakeMusic.Wav(@"C:\Users\TA\workshop\week16\Sample\MagicForest\", "tone.txt", "duration.txt", "out3.mp3", 3);
```            
# Hard
## Question: Modify given sheet
1. 變調
2. 變奏

#### Example1:
1. 讀取.../Magic/tone.txt 的樂譜
2. 將全部的升降記號#/b都取消，將全部音符還原
3. 將結果寫入new_tone.txt，再輸出一次wav檔，聽聽看是否有差別?

#### Example2:
1. 讀取.../Megalovania/duration.txt 的樂譜
2. 將全部的音符持續時間乘上1.5，讓整體節奏變慢
3. 將結果寫入new_diration.txt，再輸出一次wav檔，聽聽看是否有差別?

#### NOTE:
duration.txt / note.txt 兩者的檔案結尾，都沒有空白。
