## Demo Page
## Abstract

In recent years, emotional text-to-speech has shown considerable progress. However, it requires a large amount of labeled data, which is not easily accessible. Even if it is possible to acquire an emotional speech dataset, there is still a limitation in controlling emotion intensity. In this work, we propose a novel method for cross-speaker emotion transfer and manipulation using vector arithmetic in latent style space. By leveraging only a few labeled samples, we generate emotional speech from reading-style speech without losing the speaker identity. Furthermore, emotion strength is readily controllable using a scalar value, providing an intuitive way for users to manipulate speech. Experimental results show the proposed method affords superior performance in terms of expressiveness, naturalness, and controllability, preserving speaker identity.

## Emotion Transfer 
We transfer emotion to an emotion-neutral reading style speaker.

### Emotion transfer to a reading style speaker

| Target Emotion     | Proposed    | Style Mean    |
|   :----:    |    :----:   |     :----:    |
| Neutral     | <audio controls><source src='./assets/xtine_100shot_neutral.wav'></audio> | <audio controls><source src='./assets/xtine_base_neutral.wav'></audio>  |
| Angry       | <audio controls><source src='./assets/xtine_100shot_angry.wav'></audio> | <audio controls><source src='./assets/xtine_base_angry.wav'></audio>  |
| Sad         | <audio controls><source src='./assets/xtine_100shot_sad.wav'></audio> | <audio controls><source src='./assets/xtine_base_sad.wav'></audio>  |
| Happy       | <audio controls><source src='./assets/xtine_100shot_happy.wav'></audio> | <audio controls><source src='./assets/xtine_base_happy.wav'></audio>  |


| Target Emotion     | Proposed    | Style Mean    |
|   :----:    |    :----:   |     :----:    |
| Neutral     | <audio controls><source src='./assets/iyuno-ko-m1_100shot_neutral.wav'></audio> | <audio controls><source src='./assets/iyuno-ko-m1_base_neutral.wav'></audio> |
| Angry       | <audio controls><source src='./assets/iyuno-ko-m1_100shot_angry.wav'></audio> | <audio controls><source src='./assets/iyuno-ko-m1_base_angry.wav'></audio>  |
| Sad         | <audio controls><source src='./assets/iyuno-ko-m1_100shot_sad.wav'></audio> | <audio controls><source src='./assets/iyuno-ko-m1_base_sad.wav'></audio>  |
| Happy       | <audio controls><source src='./assets/iyuno-ko-m1_100shot_happy.wav'></audio> | <audio controls><source src='./assets/iyuno-ko-m1_base_happy.wav'></audio>  |

### One-shot emotion transfer

| Emotion     | Proposed    |
|   :----:    |    :----:   |
| Neutral     | <audio controls><source src='./assets/hamin_oneshot_neutral.wav'></audio> |
| Angry       | <audio controls><source src='./assets/hamin_oneshot_angry.wav'></audio> |
| Sad         | <audio controls><source src='./assets/hamin_oneshot_sad.wav'></audio> | 
| Happy       | <audio controls><source src='./assets/hamin_oneshot_happy.wav'></audio> |

## Ablation Study

### Proposed

| Emotion     | Proposed    |
|   :----:    |    :----:   |
| Neutral     | <audio controls><source src='./assets/nts-eng_M_prop_neutral.wav'></audio> |
| Angry       | <audio controls><source src='./assets/nts-eng_M_prop_angry.wav'></audio> | 
| Sad         | <audio controls><source src='./assets/nts-eng_M_prop_sad.wav'></audio> | 
| Happy       | <audio controls><source src='./assets/nts-eng_M_prop_happy.wav'></audio> | 

### w/o Adversarial Speaker Classifier

| Emotion     | Proposed    |
|   :----:    |    :----:   |
| Neutral     | <audio controls><source src='./assets/nts-eng_M_abl1_neutral.wav'></audio> |
| Angry       | <audio controls><source src='./assets/nts-eng_M_abl1_angry.wav'></audio> |
| Sad         | <audio controls><source src='./assets/nts-eng_M_abl1_sad.wav'></audio> |
| Happy       | <audio controls><source src='./assets/nts-eng_M_abl1_happy.wav'></audio> |

### w/o Cycle-consistency Loss

| Emotion     | Proposed    |
|   :----:    |    :----:   |
| Neutral     | <audio controls><source src='./assets/nts-eng_M_abl2_neutral.wav'></audio> |
| Angry       | <audio controls><source src='./assets/nts-eng_M_abl2_angry.wav'></audio> | 
| Sad         | <audio controls><source src='./assets/nts-eng_M_abl2_sad.wav'></audio> | 
| Happy       | <audio controls><source src='./assets/nts-eng_M_abl2_happy.wav'></audio> | 


## Controlling Emotion Strength

| Emotion     | alpha = 0.0    | alpha = 0.5 | alpha = 1.0 | alpha = 1.5 | alpha = 2.0 | 
|   :----:    |    :----:   |     :----:    |     :----:    |     :----:    |      :----:    |
| Angry       | <audio controls><source src='./assets/seungjun_angry0.wav'></audio> | <audio controls><source src='./assets/seungjun_angry0.5.wav'></audio>  | <audio controls><source src='./assets/seungjun_angry1.0.wav'></audio>  | <audio controls><source src='./assets/seungjun_angry1.5.wav'></audio>  | <audio controls><source src='./assets/seungjun_angry2.0.wav'></audio>  | 
| Sad         | <audio controls><source src='./assets/xtine_sad0.wav'></audio> | <audio controls><source src='./assets/xtine_sad0.5.wav'></audio>  | <audio controls><source src='./assets/xtine_sad1.0.wav'></audio>  | <audio controls><source src='./assets/xtine_sad1.5.wav'></audio>  | <audio controls><source src='./assets/xtine_sad2.0.wav'></audio>  |
| Happy       | <audio controls><source src='./assets/ntis-eng_F_happy0.wav'></audio> | <audio controls><source src='./assets/ntis-eng_F_happy0.5.wav'></audio>  | <audio controls><source src='./assets/ntis-eng_F_happy1.0.wav'></audio>  | <audio controls><source src='./assets/ntis-eng_F_happy1.5.wav'></audio>  | <audio controls><source src='./assets/ntis-eng_F_happy2.0.wav'></audio>  |
