# DhendyC
just another repository
public class MainActivity extends AppCompatActivity {

    private EditText angka_pertama, angka_kedua, angka_ketiga;
    private TextView hasil;
    private Button tambah, kurang, kali, bagi;
    private CheckBox satu, dua, tiga;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        angka_pertama = (EditText) findViewById(R.id.editText_angkaPertama);
        angka_kedua   = (EditText) findViewById(R.id.editText2_angkaKedua);
        angka_ketiga  = (EditText) findViewById(R.id.editText3_angkaKetiga);
        hasil         = (TextView) findViewById(R.id.textView3_hasil);
        tambah        = (Button) findViewById(R.id.button4_tambah);
        kurang        = (Button) findViewById(R.id.button5_kurang);
        kali          = (Button) findViewById(R.id.button6_kali);
        bagi          = (Button) findViewById(R.id.button7_bagi);

        final CheckBox satu = (CheckBox)findViewById(R.id.checkBox_satu);
        final CheckBox dua  = (CheckBox)findViewById(R.id.checkBox2_dua);
        final CheckBox tiga = (CheckBox)findViewById(R.id.checkBox3_tiga);

        tambah.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if((angka_pertama.getText().length()>0) && (angka_kedua.getText().length()>0) && (angka_ketiga.getText().length()>0)){
                    double angkake1 = Double.parseDouble(angka_pertama.getText().toString());
                    double angkake2 = Double.parseDouble(angka_kedua.getText().toString());
                    double angkake3 = Double.parseDouble(angka_ketiga.getText().toString());
                    double total = angkake1 + angkake2 + angkake3;
                    hasil.setText(Double.toString(total));
                }
                else{
                    Toast toast = Toast.makeText(MainActivity.this, "angka pertama, angka kedua dan angka ketiga harus dimasukan", Toast.LENGTH_LONG);
                    toast.show();
                }
            }
        });
        kali.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if ((angka_pertama.getText().length()>0) && (angka_kedua.getText().length()>0) && (angka_ketiga.getText().length()>0)){
                    double angkake1 = Double.parseDouble(angka_pertama.getText().toString());
                    double angkake2 = Double.parseDouble(angka_kedua.getText().toString());
                    double angkake3 = Double.parseDouble(angka_ketiga.getText().toString());
                    double total = angkake1 * angkake2 * angkake3;
                    hasil.setText(Double.toString(total));
                }
                else{
                    Toast toast = Toast.makeText(MainActivity.this, "angka pertama, angka kedua dan angka ketiga harus dimasukan", Toast.LENGTH_LONG);
                    toast.show();
                }
            }
        });
        kurang.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if ((angka_pertama.getText().length()>0) && (angka_kedua.getText().length()>0) && (angka_ketiga.getText().length()>0)) {
                    double angkake1 = Double.parseDouble(angka_pertama.getText().toString());
                    double angkake2 = Double.parseDouble(angka_kedua.getText().toString());
                    double angkake3 = Double.parseDouble(angka_ketiga.getText().toString());
                    double total = angkake1 - angkake2 - angkake3;
                    hasil.setText(Double.toString(total));
                }
                else{
                    Toast toast = Toast.makeText(MainActivity.this, "angka pertama, angka kedua dan angka ketiga harus dimasukan", Toast.LENGTH_LONG);
                    toast.show();
                }
            }
        });
        bagi.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                if ((angka_pertama.getText().length()>0) && (angka_kedua.getText().length()>0) && (angka_ketiga.getText().length()>0)){
                    double angkake1 = Double.parseDouble(angka_pertama.getText().toString());
                    double angkake2 = Double.parseDouble(angka_kedua.getText().toString());
                    double angkake3 = Double.parseDouble(angka_ketiga.getText().toString());
                    double total = angkake1 / angkake2 / angkake3;
                    hasil.setText(Double.toString(total));
                }
                else{
                    Toast toast = Toast.makeText(MainActivity.this, "angka pertama, angka kedua dan angka ketiga harus dimasukan", Toast.LENGTH_LONG);
                    toast.show();
                }
            }
        });
        if (satu.isChecked() && dua.isChecked() && tiga.isChecked()){
            angka_pertama.getText().toString();
            angka_kedua.getText().toString();
            angka_ketiga.getText().toString();
            hasil.setText(toString().trim());
        }

        }
    }
