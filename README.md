# XylophoneApp
Simple XylophoneApp by using SoundPool & SoundPool.Builder object

   #Java_Skill_Covered: SoundPool & SoundPool.Builder

        // TODO: Create a new SoundPool
        if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.LOLLIPOP){
            AudioAttributes audioAttributes = new AudioAttributes.Builder()
                    .setContentType(AudioAttributes.CONTENT_TYPE_MUSIC)
                    .setUsage(AudioAttributes.USAGE_MEDIA)
                    .build();
            mSoundPool = new SoundPool.Builder()
                    .setMaxStreams(NR_OF_SIMULTANEOUS_SOUNDS)  // (7)
                    .setAudioAttributes(audioAttributes)
                    .build();
        }else
        {
            mSoundPool = new SoundPool(NR_OF_SIMULTANEOUS_SOUNDS, AudioManager.STREAM_MUSIC,0);
        }

#XML_Skill-Covered: Style Sheet in Values folder for activity_main.xml file
   
   Example:
   <style name="keyStyle">
        <item name="android:layout_weight">1</item>
        <item name="android:layout_marginTop">3dp</item>
        <item name="android:layout_marginBottom">3dp</item>
    </style>

    <Button
        android:id="@+id/c_key"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        style="@style/keyStyle"
        android:onClick="playC"
        android:background="@color/red" />
    
    
    
    



