# XylophoneApp
Simple XylophoneApp by using SoundPool object
public class MainActivity extends AppCompatActivity {
    // Helpful Constants
    private final int NR_OF_SIMULTANEOUS_SOUNDS = 7;
    private final float LEFT_VOLUME = 1.0f;
    private final float RIGHT_VOLUME = 1.0f;
    private final int NO_LOOP = 0;
    private final int PRIORITY = 0;
    private final float NORMAL_PLAY_RATE = 1.0f;

    // TODO: Add member variables here
    private SoundPool mSoundPool;
    private int mCSoundId;
    private int mDSoundId;
    private int mESoundId;
    private int mFSoundId;
    private int mGSoundId;
    private int mASoundId;
    private int mBSoundId;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // TODO: Create a new SoundPool
        mSoundPool = new SoundPool(NR_OF_SIMULTANEOUS_SOUNDS, AudioManager.STREAM_MUSIC,0);


        // TODO: Load and get the IDs to identify the sounds
        mCSoundId = mSoundPool.load(getApplicationContext(),R.raw.note1_c, 1);
        mDSoundId = mSoundPool.load(getApplicationContext(), R.raw.note2_d, 1);
        mESoundId = mSoundPool.load(getApplicationContext(), R.raw.note3_e, 1);
        mFSoundId = mSoundPool.load(getApplicationContext(), R.raw.note4_f, 1);
        mGSoundId = mSoundPool.load(getApplicationContext(),R.raw.note1_c, 1);
        mASoundId = mSoundPool.load(getApplicationContext(),R.raw.note6_a, 1);
        mBSoundId = mSoundPool.load(getApplicationContext(),R.raw.note7_b, 1);
    }

    // TODO: Add the play methods triggered by the buttons
    public void playC(View view){
        mSoundPool.play(mCSoundId, LEFT_VOLUME, RIGHT_VOLUME, PRIORITY, NO_LOOP,NORMAL_PLAY_RATE);

    }
    public void playD(View view){
        mSoundPool.play(mDSoundId, LEFT_VOLUME, RIGHT_VOLUME, PRIORITY, NO_LOOP,NORMAL_PLAY_RATE);

    }
    public void playE(View view){
        mSoundPool.play(mESoundId, LEFT_VOLUME, RIGHT_VOLUME, PRIORITY, NO_LOOP,NORMAL_PLAY_RATE);

    }
    public void playF(View view){
        mSoundPool.play(mFSoundId, LEFT_VOLUME, RIGHT_VOLUME, PRIORITY, NO_LOOP,NORMAL_PLAY_RATE);

    }
    public void playG(View view){
        mSoundPool.play(mGSoundId, LEFT_VOLUME, RIGHT_VOLUME, PRIORITY, NO_LOOP,NORMAL_PLAY_RATE);

    }
    public void playA(View view){
        mSoundPool.play(mASoundId, LEFT_VOLUME, RIGHT_VOLUME, PRIORITY, NO_LOOP,NORMAL_PLAY_RATE);

    }
    public void playB(View view){
        mSoundPool.play(mBSoundId, LEFT_VOLUME, RIGHT_VOLUME, PRIORITY, NO_LOOP,NORMAL_PLAY_RATE);

    }
}



<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="5dp"
    tools:context=".MainActivity">
    <Button
        android:id="@+id/c_key"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        style="@style/keyStyle"
        android:onClick="playC"
        android:background="@color/red" />
    <Button
        android:id="@+id/d_key"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        style="@style/keyStyle"
        android:layout_marginRight="5dp"
        android:layout_marginLeft="5dp"
        android:onClick="playD"
        android:background="@color/orange" />
    <Button
        android:id="@+id/e_key"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        style="@style/keyStyle"
        android:layout_marginRight="10dp"
        android:layout_marginLeft="10dp"
        android:onClick="playE"
        android:background="@color/yellow" />
    <Button
        android:id="@+id/f_key"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        style="@style/keyStyle"
        android:layout_marginRight="15dp"
        android:layout_marginLeft="15dp"
        android:onClick="playF"
        android:background="@color/green" />
    <Button
        android:id="@+id/g_key"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        style="@style/keyStyle"
        android:layout_marginRight="20dp"
        android:layout_marginLeft="20dp"
        android:onClick="playG"
        android:background="@color/turquoise" />
    <Button
        android:id="@+id/a_key"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        style="@style/keyStyle"
        android:layout_marginRight="25dp"
        android:layout_marginLeft="25dp"
        android:onClick="playA"
        android:background="@color/blue" />
    <Button
        android:id="@+id/b_key"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        style="@style/keyStyle"
        android:layout_marginRight="30dp"
        android:layout_marginLeft="30dp"
        android:onClick="playB"
        android:background="@color/purple" />



