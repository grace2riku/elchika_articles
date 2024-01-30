# ライセンス
## LGPL-2.1 license
つぎのファイルは **【LGPL-2.1 license】** です。

* CatMoeller/Main_Rover_PID_Adjustment/Main_Rover_PID_Adjustment.ino
* CatMoeller/Main_Rover_PID_Adjustment/pwm_control.ino

ベースにしたつぎのリポジトリのライセンスと同様です。

* https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/tree/main/Sketches/SprTurtleBot_PID_Adjustment/Main_Rover_PID_Adjustment

## MIT license
上記以外のソースコードは **【MIT license】** です。

# Spresenseモーラーについて
Spresenseがモーターを駆動し、モーラーをランダムなスピード・方向に動かします。

猫を楽しませるためのロボットです。次の図がSpresenseモーラーの全体写真です。


# 部品
Spresenseモーラーの使用部材です。
SpresenseモーラーはつぎのGitHubのローバー**SprTurtleBot**をベースに製作しました。

バガスどんぶり + モーラーを取り付ける駆動部はSprTurtleBotのハードウェアをそのまま流用しています。

https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/blob/main/Documents/Spresense%20%E3%81%A8micro-ROS%20%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E3%83%AD%E3%83%9C%E3%83%83%E3%83%88%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0.pdf


| No | 部品 | 個数 | 役割 | 備考 |
| :--- | :--- | :--- | :--- | :--- |
| 1 | Spresense メインボード | 1 | モーラーのコントローラ | SPRESENSEメインボード[CXD5602PWBMAIN1](https://www.switch-science.com/products/3900) |
| 2 | Spresense 拡張ボード | 1 | IOボード | SPRESENSE拡張ボード[CXD5602PWBEXT1](https://www.switch-science.com/products/3901) |
| 3 | 台座+モーター+タイヤキット | 1 | 基本シャーシ | [2WDロボットスマートカーシャーシ 2輪駆動 DIY教材](https://www.amazon.co.jp/gp/product/B01IWHE9VI/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1) |
| 4 | エンコーダー | 2 | タイヤの回転数をカウント | [IR赤外線スロット付きオプトカプラーモーター速度検出](https://www.amazon.co.jp/gp/product/B084VP1GXS/ref=ppx_yo_dt_b_asin_title_o03_s00?ie=UTF8&psc=1) |
| 5 | モータードライバ | 1 | モーター駆動用回路 | [DRV8835使用ステッピング&DCモータドライバモジュール](https://akizukidenshi.com/catalog/g/g109848/) |
| 6 | ブレッドボード | 1 | 配線の中継 |  |
| 7 | ワイヤー | 多数 |  |  |
| 8 | モバイルバッテリー | 1 |  |  |
| 9 | Micro USB(USB A-MicroB)ケーブル | 1 | モバイルバッテリーからSpresenseに給電するために必要 |  |
| 10 | モーラー | 1 | 猫の興味を引く | [オリジナル　モーラー　パープル](https://item.rakuten.co.jp/auc-ookawaya/4979092016953/?s-id=pc_shop_recommend&rtg=c1e67285c7003768080607e3d6635f69) |
| 11 | バガスどんぶり | 1 | モーラーの取り付けと配線を隠す | [電子レンジに使えるバガスどんぶり](https://jp.daisonet.com/products/4550480309866) |
| 12 | つまようじ | 1 | モーラーのテグスを巻き、どんぶりに固定する |  |
| 13 | ネジ | 2 | ネジ・ワッシャー・ナットで台座とエンコーダーを固定する |  |
| 14 | ワッシャー | 2 |  |  |
| 15 | ナット | 2 |  |  |


# 設計図
Spresenseモーラーは前述したとおり**SprTurtleBot**をベースにしています。
必要な設計図はつぎのGitHub資料に記載されていたので流用します。

[Spresense とmicro-ROS ではじめるロボットプログラミング.pdf](https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/blob/main/Documents/Spresense%20%E3%81%A8micro-ROS%20%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E3%83%AD%E3%83%9C%E3%83%83%E3%83%88%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0.pdf)

# 組み立て
## エンコーダーの取り付け
エンコーダーの取り付けはNo. 13, 14, 15のネジ、ワッシャー、ナットで行います。

このネジ・ワッシャー・ナットは部品表No.3の台座+モーター+タイヤキット、No.4のエンコーダーに付属していません。個別に購入または調達する必要があります。

下図は台座表面の写真です。エンコーダーの片側だけネジを挿入しています。もう一方はモーターとぶつかり固定できません。そのためエンコーダーの固定は2箇所のうち1つとします。

下図は台座裏面の写真です。ワッシャー、ナットで固定しています。

## どんぶりとモーラーの取り付け
モーラーはどんぶりに取り付けます。モーラーを取り付けたどんぶりは配線を隠すように被せます。
モーラーとどんぶりを取り付けは下図になります。

モーラーとどんぶりの取り付け手順はつぎのとおりです。

どんぶりにはキリなどで穴を開けます。
モーラーは透明なテグスがついています。
どんぶりに開けた穴にテグスをとおします。
テグスを適度な長さにしたら、半分におった爪楊枝にテグスを巻き付けます。
テグスを巻き付けた爪楊枝とどんぶりをテープなどで固定します。
モーラーを取り付けたどんぶりで配線を隠して組み立て完成です。

# 配線
## 配線図
下図は[Spresense とmicro-ROS ではじめるロボットプログラミング.pdf](https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/blob/main/Documents/Spresense%20%E3%81%A8micro-ROS%20%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E3%83%AD%E3%83%9C%E3%83%83%E3%83%88%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0.pdf)のp56からの引用した配線図です。このとおりに配線していきます。

### 配線図とモーラー実体との対応
モーラーはSpresenseメインボードと拡張ボードの**SONY**のシルクの向きを配線図と合わせます。向きを合わせたら配線図のとおりに配線してきます。

### モーター（AOUT2, BOUT2）の配線について
モーター（AOUT2, BOUT2）の配線は下図のようにモータ上側の端子（ケースに近い方）と接続します（赤の配線がAOUT2, BOUT2）。

### 電源の配線について
配線図では電源は基板で分配されています。今回は電源分配用基板を使わず、ブレッドボードで電源ラインを分配します。


# ソースコード
SpresenseモーラーのソースコードはつぎのGitHubリポジトリに格納しています。

* https://github.com/grace2riku/cat_moeller_spresense

開発環境はArduino IDEです。

## Spresenseモーラーの責務
Spresenseモーラーのメインの責務はつぎの2つです。

* モーター駆動パラメータを生成する
* モーター駆動パラメータでモーターを駆動する

モーター駆動パラメータはつぎになります。
* 移動スピード（0〜1.0(m/s) ）
* 移動方向（前進・後進・右回り・左回り）

## ベースにしたソースコード
Spresenseモーターはつぎのプログラムをベースにしています。

* [Spresense とmicro-ROS ではじめるロボットプログラミング.pdf](https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/blob/main/Documents/Spresense%20%E3%81%A8micro-ROS%20%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E3%83%AD%E3%83%9C%E3%83%83%E3%83%88%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0.pdf)のp64 **SprTurtleBot のPID調整プログラム**

### プログラムの概要
プログラムの概要はp64から引用した下図を参照してください。

各ブロックはつぎの役割があります。
* メインコアはpythonプログラム→サブコアから伝達されたモーター駆動パラメータを受信する
* メインコアは受信したパラメータに従いモーターを駆動する
* サブコアはpythonプログラムからWifiでモーター駆動パラメータを受信する
* サブコアはモーター駆動パラメータをコア間通信でメインコアに送信する
* pythonプログラムはユーザーから入力されたモーター駆動パラメータをWifiでサブコアに送信する

### ソースコードの構成
PID調整プログラムのSpresenseソースコードはメインコアとサブコアの2つになります。

メインコアのGitHubリポジトリはこちらです。
* https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/tree/main/Sketches/SprTurtleBot_PID_Adjustment/Main_Rover_PID_Adjustment

サブコアのGitHubリポジトリはこちらです。
* https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/tree/main/Sketches/SprTurtleBot_PID_Adjustment/Sub_WiFi_Connection


## ベースのソースコードからの変更点
下図はSpresenseモーラーのソフトウェアをブロック図で表しています。

ベースにしたコードとつぎの点が違います。
1. Ubuntuとpythonプログラムがない
2. サブコア1はWi-Fiを使わない

### Ubuntuとpythonプログラムがない
SpresenseモーラーはPC不要でハードウェアのみで動作するようにしたかったため、Ubuntuとpythonプログラムが不要になりました。

サブコア1でモーター駆動のパラメーターをランダムで生成します。

サブコア1は1.5秒周期でメインコアにコア間通信で生成したモーター駆動パラメーターを送信します。

**モーター駆動パラメータ**はつぎの項目です。
* 移動スピード
  * -1.0〜1.0(m/s)の範囲からランダム値で決定する（0 <= 1は前進、-1 <= 0は後進）
* 移動方向
  * 前進・後進（0）、右回り（-1）、左回り（1）の範囲からランダムで決定する

サブコア1はPID係数もコア間通信で送信していますが、固定値としています。
* KP = 120
* KI = 30
* KD = 3

本当はPID係数はSpresnseモーラーの動作環境によって調整すると思いますが今回は固定値としました。

PID係数は参考資料[Spresense とmicro-ROS ではじめるロボットプログラミング.pdf](https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/blob/main/Documents/Spresense%20%E3%81%A8micro-ROS%20%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E3%83%AD%E3%83%9C%E3%83%83%E3%83%88%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0.pdf)のp69以降の**SprTurtleBotのプログラム**のGitHubリポジトリの設定値を使うことにしました。

SprTurtleBotのGitHubリポジトリ:

https://github.com/TE-YoshinoriOota/Spresense-microROS-Seminar/blob/main/Sketches/SprTurtleBot/Sub_Rover_Control/Sub_Rover_Control.ino


### サブコア1はWi-Fiを使わない
ベースのソースコードはサブコア1がWi-Fi経由でpythonプログラムからパラメータを受信していました。

pythonプログラムが不要になり、サブコア1自身でパラメータを生成するようにしたのでWi-Fiのインタフェースも不要になりました。


## ソースコードの配置
ソースコードはつぎの配置になっています。

### モーター駆動
モーター駆動のソースコードはつぎになります。

* CatMoeller/Main_Rover_PID_Adjustment
  * Main_Rover_PID_Adjustment.ino
  * pwm_control.ino

モータ駆動のコードはメインコアに配置します。


### モーター駆動のパラメータ生成
モーター駆動のパラメータ生成のソースコードはつぎになります。

* RandomParameterCreater/cat_moeller_spresense
  * src/ntshell
  * RandomParameterCreater.cpp
  * RandomParameterCreater.h
  * cat_moeller_spresense.ino
  * usrcmd_cat_moeller_spresense.cpp

モーター駆動のパラメータ生成はサブコア1に配置します。


## モーター駆動（メインコアに配置）のソースコード

```cpp:Main_Rover_PID_Adjustment.ino
#ifdef SUBCORE
#error "Core selection is wrong!!"
#endif

#include <MP.h>
#include <MPMutex.h>
MPMutex mutex(MP_MUTEX_ID0);

const int R0 = 0; // pwm0 - 6 pin
const int R1 = 1; // pwm1 - 5 pin
const int L0 = 2; // pwm2 - 9 pin
const int L1 = 3; // pwm3 - 3 pin

#define R_EN 10
#define L_EN 11
#define DELAY_TIME 40
#define MOTOR_SW 12

#define TORQUE_COMP_POWER 255
#define TORQUE_COMP_TIME_R 5
#define TORQUE_COMP_TIME_L 5

#define KP 0
#define KI 0
#define KD 0
 
float R_Kp = KP; 
float R_Ki = KI;
float R_Kd = KD;
float L_Kp = KP;
float L_Ki = KI; 
float L_Kd = KD;
float VRt = 0.0;
float VLt = 0.0;

int32_t R_duty = 0;
int32_t L_duty = 0;

const int recv_buf_size = 32;
char recv_buf[recv_buf_size] = {0};
bool param_updated = false;
  
volatile uint32_t R = 0;
volatile uint32_t L = 0;
void Encoder0() {  ++R; }
void Encoder1() {  ++L; }

struct pid_data {
  float rKp;
  float rKi;
  float rKd;
  float lKp;
  float lKi;
  float lKd;
  float vt;
  float rot;
};

struct torque_data {
  int R_duty;
  int L_duty;
};

const int subcore = 1;

struct pid_data* pid;
struct torque_data td;

float calc_speed(uint32_t enc_count, uint32_t duration_ms, float* mileage, float target) {
  static const float D  = 0.0325; // tire radius (m)
  static const float Enc_Theta = 9.0;  // a unit degree of the edge encoder 
  if (duration_ms == 0.0) { *mileage = 0.0; return 0.0; } 
  float rotation_ = enc_count*Enc_Theta;  // rotation (degree)
  float rot_radian_ = PI*rotation_/180.0; // convert dgree to radian
  float mileage_ = rot_radian_*D; // (m)
  float rov_speed_ = mileage_*1000.0/(float)(duration_ms); 
  //MPLog("%d,%f,%f,%f\n", enc_count, rotation_, mileage_, rov_speed_);
  *mileage = mileage_;
  if (target < 0) rov_speed_ = -rov_speed_; 
  return rov_speed_;
}

void setup() {
  Serial.begin(115200);
    
  pinMode(MOTOR_SW, OUTPUT);
  digitalWrite(MOTOR_SW, LOW);
  attachInterrupt(R_EN, Encoder0, CHANGE);
  attachInterrupt(L_EN, Encoder1, CHANGE);

  // setup pwm pins
  setup_pwm(0);
  setup_pwm(1);
  setup_pwm(2);
  setup_pwm(3);

  MP.begin(subcore);
  MP.RecvTimeout(MP_RECV_POLLING);
  /* Disable console for SubCore to use it */
  MP.DisableConsole();

  // motor power on
  digitalWrite(MOTOR_SW, HIGH);

}

void loop() {
  static uint32_t start_time = 0;
  static uint32_t last_time = 0;
  static float R_last_err = 0.0;
  static float L_last_err = 0.0;
  static float R_err_integ = 0.0;
  static float L_err_integ = 0.0; 
  static const float d = 0.065; /* (the legnth of chassis)/2 (m) */ 
  int8_t snd_id;

  float R_Vm, L_Vm;  // actual speeds calcurated by encorders

  static const bool debug = false;

  int8_t recv_id;
  int ret = MP.Recv(&recv_id, &pid, subcore);
  if (ret > 0) {
    R_Kp = pid->rKp; 
    R_Ki = pid->rKi;
    R_Kd = pid->rKd;
    L_Kp = pid->lKp;
    L_Ki = pid->lKi; 
    L_Kd = pid->rKd;
    if (pid->rot == 0.0) {
      VRt = VLt = pid->vt;
    } else if (pid->rot > 0.0) {
      VRt = +pid->vt;
      VLt = -pid->vt;
    } else if (pid->rot < 0.0) {
      VRt = -pid->vt;
      VLt = +pid->vt;
    }
    MPLog("param(orig) = %f,%f,%f,%f,%f,%f,%f,%f\n",
      pid->rKp,pid->rKi,pid->rKd,pid->lKp,pid->lKi,pid->rKd,pid->vt, pid->rot); 

    MPLog("param(copy) = %f,%f,%f,%f,%f,%f,%f,%f\n",
      R_Kp,R_Ki,R_Kd,L_Kp,L_Ki,L_Kd,VRt,VLt); 
    start_time = millis();
  }
 
  uint32_t current_time = millis();
  uint32_t duration = current_time - last_time; 
  last_time = current_time;    

  float R_err  = 0.0;
  float L_err  = 0.0;
  float R_derr = 0.0;
  float L_derr = 0.0;

  if (current_time - start_time > 1000) {
    // MPLog("Stop TurtleBotSpr\n"); 
    pwm_control(0, 0); // backward
    pwm_control(1, 0); // forward
    pwm_control(2, 0); // backward
    pwm_control(3, 0); // forward
    VRt = VLt = 0.0;   
    R_Vm = L_Vm = 0.0;
    R_duty = L_duty = 0;
    R_last_err = L_last_err = 0.0;
    R_err_integ = L_err_integ = 0.0;
    delay(DELAY_TIME);
    return;
  }

  if (debug) {
    MPLog("R_err_integ: %f, L_err_integ: %f, R_last_err: %f, L_last_err: %f\n",
      R_err_integ, L_err_integ, R_last_err, L_last_err);
  }

  noInterrupts();
  uint32_t cur_R = R; R = 0; 
  uint32_t cur_L = L; L = 0;
  interrupts();
  float R_mileage = 0.0;
  float L_mileage = 0.0;
  
  R_Vm = calc_speed(cur_R, duration, &R_mileage, VRt);
  L_Vm = calc_speed(cur_L, duration, &L_mileage, VLt); 
  if (debug) {
    MPLog("%d,%d,%d,%f,%f,%f,%f,%f,%f,%f,%f\n",
      duration,cur_R,cur_L,VRt,VLt,R_Vm,L_Vm,R_mileage,L_mileage,VRt,VLt); 
  }

  float duration_sec = duration/1000.0;
  R_err        = VRt - R_Vm;
  L_err        = VLt - L_Vm;
  R_err_integ += (R_err + R_last_err)*0.5*duration_sec;
  L_err_integ += (L_err + L_last_err)*0.5*duration_sec;
  R_derr       = (R_err - R_last_err)/duration_sec;  
  L_derr       = (L_err - L_last_err)/duration_sec;

  if (debug) {
    MPLog("R_Kp: %f, R_Ki: %f, R_Kd: %f,L_Kp: %f, L_Ki: %f, L_Kd: %f\n",
        R_Kp, R_Ki, R_Kd, L_Kp, L_Ki, L_Kd);
    MPLog("R_err: %f, L_err: %f, R_err_integ: %f, L_err_integ: %f, R_derr: %f, L_derr: %f\n",
        R_err, L_err, R_err_integ, L_err_integ, R_derr, L_derr);
  }


  R_duty = (int32_t)(R_Kp*R_err + R_Ki*R_err_integ + R_Kd*R_derr);
  L_duty = (int32_t)(L_Kp*L_err + L_Ki*L_err_integ + L_Kd*L_derr);

  if (abs(R_duty) > 255) {
    if (debug) MPLog("Over range on R: %d\n", R_duty);
    if (R_duty > 255)    R_duty = +255;
    else if (R_duty < 0) R_duty = -255;
  }

  if (abs(L_duty) > 255) {
    if (debug) MPLog("Over range on L: %d\n", L_duty);
    if (L_duty > 255)    L_duty = +255;
    else if (L_duty < 0) L_duty = -255;
  }

  R_last_err = R_err;
  L_last_err = L_err;   

  MPLog("R_duty: %d, L_duty: %d\n", R_duty, L_duty);
  td.R_duty = R_duty;
  td.L_duty = L_duty;
//  int8_t snd_id = 101;
  snd_id = 101;
  MP.Send(snd_id, &td, subcore);
  
  if (R_Vm == 0.0 && VRt != 0.0) {
    // Torque Compensation
    if (VRt > 0.0) {
      pwm_control(0, 0);                 // backward
      pwm_control(1, TORQUE_COMP_POWER); // forward
    } else if (VRt < 0.0) {
      pwm_control(1, TORQUE_COMP_POWER); // backward
      pwm_control(0, 0);                 // forward
    }
    delay(TORQUE_COMP_TIME_R);
  };
  
  if (VRt > 0.0) {
    pwm_control(0, 0);           // backward
    pwm_control(1, abs(R_duty)); // forward
  } else if (VRt < 0.0) {
    pwm_control(0, abs(R_duty)); // backward
    pwm_control(1, 0);           // forward
  } else if (VRt == 0.0) {
    pwm_control(0, 0);           // backward
    pwm_control(1, 0);           // forward
  }

  if (L_Vm == 0.0 && VLt != 0.0) {
    // Torque Compensation
    if (VRt > 0.0) {
      pwm_control(2, 0);                 // backward
      pwm_control(3, TORQUE_COMP_POWER); // forward
    } else if (VRt < 0.0) {
      pwm_control(2, TORQUE_COMP_POWER); // backward
      pwm_control(3, 0);                 // forward
    }
    delay(TORQUE_COMP_TIME_L);
  };  

  if (VLt > 0.0) {
    pwm_control(2, 0);           // backward
    pwm_control(3, abs(L_duty)); // forward
  } else if (VLt < 0.0) {
    pwm_control(2, abs(L_duty)); // backward
    pwm_control(3, 0);           // forward    
  } else if (VLt == 0.0) {
    pwm_control(2, 0);           // backward
    pwm_control(3, 0);           // forward     
  }

  delay(DELAY_TIME);
}
```

```cpp:pwm_control.ino
#include <sys/ioctl.h>
#include <stdio.h>
#include <fcntl.h>   
#include <nuttx/timers/pwm.h>


int fd0;
int fd1;
int fd2;
int fd3;

struct pwm_info_s info;


void setup_pwm(int pwm_num) {

  int fd;
  switch(pwm_num) {
  case 0:
    Serial.println("setup /dev/pwm0");
    fd0 = open("/dev/pwm0", O_RDONLY);
    fd = fd0;
    break;
  case 1:
    Serial.println("setup /dev/pwm1");
    fd1 = open("/dev/pwm1", O_RDONLY);
    fd = fd1;
    break;
  case 2:
    Serial.println("setup /dev/pwm2");
    fd2 = open("/dev/pwm2", O_RDONLY);
    fd = fd2;
    break;
  case 3:
    Serial.println("setup /dev/pwm3");
    fd3 = open("/dev/pwm3", O_RDONLY);
    fd = fd3;
    break;
  default:
    Serial.println("invalid pwm num");
    return;
  }
  
  info.frequency = 500; // Hz
  info.duty      = 0x0000;
  ioctl(fd, PWMIOC_SETCHARACTERISTICS, (unsigned long)((uintptr_t)&info));
  ioctl(fd, PWMIOC_START, 0);
}

void pwm_control(int pwm_num, uint32_t duty) {
  int fd;
  switch (pwm_num) {
  case 0: fd = fd0; break;
  case 1: fd = fd1; break;
  case 2: fd = fd2; break;
  case 3: fd = fd3; break;
  default:
    Serial.println("invalid pwm num");
    return;
  }
  
  info.duty = map(duty, 0x00, 0xff, 0x0000, 0xffff);
  ioctl(fd, PWMIOC_SETCHARACTERISTICS, (unsigned long)((uintptr_t)&info));
  ioctl(fd, PWMIOC_START, 0);
}
```

## モーター駆動のパラメータ生成（サブコア1に配置）のソースコード

```cpp:cat_moeller_spresense.ino
#ifndef SUBCORE
#error "Core selection is wrong!!"
#endif

#include <MP.h>

#include "src/ntshell/ntshell.h"
extern "C" {
#include "src/ntshell/ntshell_spresense_arduino.h"
}
#include "src/ntshell/usrcmd_cat_moeller_spresense.h"
#include "RandomParameterCreater.h"

#define PROMPT_STR ">"

#define DELAY_TIME (40)
#define DRIVE_PARAMETER_SEND_INTERVAL 1500000

static ntshell_t ntshell;

struct pid_data {
  float rKp;
  float rKi;
  float rKd;
  float lKp;
  float lKi;
  float lKd;
  float vt;
  float rot;
};

struct torque_data {
  int R_duty;
  int L_duty;
};


static int func_read(char* buf, int cnt, void* extobj) {
  if (Serial.available())
    return Serial.readBytes(buf, cnt);
  else
    return 0;
}

static int func_write(const char* buf, int cnt, void* extobj) {
  return Serial.write((uint8_t*)buf, cnt);
}

static int func_callback(const char* text, void* extobj) {
  return usrcmd_execute(text);
}

unsigned int drive_parameter_send() {
    digitalWrite(LED0, LOW);
    digitalWrite(LED1, HIGH);

    struct pid_data pid;
    pid.rKp = pid.lKp = 120;
    pid.rKi = pid.lKi = 30;
    pid.rKd = pid.lKd = 3;

    struct random_parameter val;
    val = random_parameter_create();
    pid.vt = val.vt;
    pid.rot = val.rot;

    int8_t snd_id = 100;
    MP.Send(snd_id, &pid);    

  return DRIVE_PARAMETER_SEND_INTERVAL;
}

void setup() {
  // put your setup code here, to run once:
  random_parameter_initialize();

  MP.begin();
  MP.RecvTimeout(MP_RECV_POLLING); 
  MP.EnableConsole();
  
  Serial.begin(115200);
  while (!Serial) {
    ;;
  }

  ntshell_init(
    &ntshell,
    func_read,
    func_write,
    func_callback,
    (void *)(&ntshell));

  ntshell_set_prompt(&ntshell, PROMPT_STR);

  Serial.println("Wellcome to Spresense Arduino.\r\n type 'help' for help.");
  Serial.print(PROMPT_STR);
  Serial.flush();

  attachTimerInterrupt(drive_parameter_send, DRIVE_PARAMETER_SEND_INTERVAL);  
}

void loop() {
  // put your main code here, to run repeatedly:
  while(Serial.available())
    ntshell_execute_spresense_arduino(&ntshell);

  int8_t rid;

  struct torque_data td;
  int ret = MP.Recv(&rid, &td);
  if (ret == 101) {
    digitalWrite(LED0, HIGH);
    digitalWrite(LED1, LOW);
  }

  usleep(DELAY_TIME*1000);
}
```

```cpp:RandomParameterCreater.cpp
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include "RandomParameterCreater.h"

void random_parameter_initialize(void) {
  srand(time(NULL));
}

struct random_parameter random_parameter_create(void) {
  struct random_parameter val;

  // Speed(m/s)の乱数生成 -1.0〜1.0
  val.vt = 2.0f * ((float)rand() / (float)RAND_MAX) - 1.0f;

  // Rotの乱数生成 -1, 0, 1
  val.rot = rand() % 3 - 1;

  return val;
}
```

# 動作の様子
Spresenseモーラーが動作している様子です。

@[youtube](https://youtube.com/shorts/9DEYoG3bVgM)
