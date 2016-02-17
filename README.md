# SimpleDB-android
  The simple way to manage sharedpreference android
  
# Requirements 
  1. [google-gson](https://github.com/google/gson)

# How to use

  ```
  public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        // initialize
        SimpleDB simpleDB = new SimpleDB(this);

        // array of string
        ArrayList<String> array = new ArrayList<>();
        simpleDB.putList("ARRAYLIST", array);
        array = simpleDB.getList("ARRAYLIST");

        // put string
        simpleDB.putString("STRING", "value");
        String value = simpleDB.getString("STRING");

        // put boolean
        simpleDB.putBoolean("BOOLEAN", true);
        boolean isTrue = simpleDB.getBoolean("BOOLEAN");

        // put array of boolean
        boolean bool[] = new boolean[4];
        simpleDB.putBooleanArray("BOOLEAN_ARRAY", bool);
        bool = simpleDB.getBooleanArray("BOOLEAN_ARRAY");

        // put double
        simpleDB.putDouble("DOUBLE", 0.2);
        double a = simpleDB.getDouble("DOUBLE");

        // put float
        simpleDB.putFloat("FLOAT", 0.25f);
        float b = simpleDB.getFloat("FLOAT");

        // put hashmap<String, String>
        HashMap<String, String> hashMap = new HashMap<>();
        simpleDB.putHashMap("HASHMAP", hashMap);
        hashMap = simpleDB.getHashmap("HASHMAP");

        // put integer
        simpleDB.putInt("INTEGER", 20);
        int c = simpleDB.getInt("INTEGER");

        // put arraylist of boolean
        ArrayList<Boolean> booleans = new ArrayList<>();
        simpleDB.putListBoolean("LIST_BOOLEAN", booleans);
        booleans = simpleDB.getListBoolean("LIST_BOOLEAN");

        // put arraylist of integer
        ArrayList<Integer> integers = new ArrayList<>();
        simpleDB.putListInt("LIST_INTEGER", integers);
        integers = simpleDB.getListInt("LIST_INTEGER");

        // put arraylist of hashmap<String, String>
        ArrayList<HashMap<String, String>> hashMaps = new ArrayList<>();
        simpleDB.putListHashMap("LIST_HASHMAP", hashMaps);
        hashMaps = simpleDB.getListHashmap("LIST_HASHMAP");

        // put long
        simpleDB.putLong("LONG", 10000);
        long d = simpleDB.getLong("LONG");

        // put object
        DummyClass dummyClass = new DummyClass();
        dummyClass.setAddress("address");
        dummyClass.setName("name");
        simpleDB.putObject("DUMMY", dummyClass);
        simpleDB.getObject("DUMMY", DummyClass.class);
        
        // clear
        simpleDB.remove("KEY");

        // clear all
        simpleDB.clear();

    }
  }
  ```
# Credits
  Thanks to [google-gson](https://github.com/google/gson) :)
