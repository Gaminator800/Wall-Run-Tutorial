# Wall-Run-Tutorial
 
This is how you will make your player Wall Run for your game this is based on a YouTube Tutorial I've watched.
I hope this will help you too.

## 1. Create two walls and then create two invisible platforms on each wall.
![Two Walls ScreenShot](https://github.com/LSBUGPG/Vision/assets/17784224/258f7007-9407-4dea-9a07-d6cf654882d1)

Make sure you make them invisible.

![PlatformScreenShot](https://github.com/LSBUGPG/Vision/assets/17784224/7d48c85a-0cc0-4fce-a5df-b605b5d5bc1a)

## 2. If you have a scripts folder then you create a script called `WallRunScript`.
![WallRunScriptScreenShot](https://github.com/LSBUGPG/Vision/assets/17784224/1f916629-cfaf-421f-b215-96cb1bb0482c)

## 3. Open up the Script.
Once you open it you will put in this code make sure you put the bool spelled correctly.
```.cs
    public GameObject Platform;
    public GameObject Platform2;
    public bool isOn = false;
```

## 4. Add the input key in the Void Update section for `WallRun` and `Stop`.
```.cs
    void Update()
    {
        if (Input.GetKey("f"))
        {
            StartCoroutine(WallRun());
        }

        if (Input.GetKeyUp("f"))
        {
            StartCoroutine(Stop());
        }
    }
```

## 5.Add two Enumerators for `WallRun` and `Stop`.
```.cs
    IEnumerator WallRun()
    {
        isOn = true;
        Platform.SetActive(true);
        Platform2.SetActive(true);
        yield return new WaitForSeconds(0f);
    }

    IEnumerator Stop()
    {
        isOn = false;
        Platform.SetActive(false);
        Platform2.SetActive(false);
        yield return new WaitForSeconds(0f);
    }
```

## 6. Then PlayTest the game and then there you have a character that can wall run on anytging.
Special Thanks to Noblob for the tutorial I've followed.

Channel: https://www.youtube.com/@NoblobRS
Video Tutorial: https://www.youtube.com/watch?v=5jTAEUz8sn8

Hope you've found this useful let me know what you think.
