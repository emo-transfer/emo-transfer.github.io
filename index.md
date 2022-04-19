## Audio Samples from "Vector Arithmetic in Latent Style Space for Emotion Transfer"

### Abstract

Emotion in speech plays an important role in human dialogue. Without emotion, it is hard to generate truly human-like
speech. In recent years, emotional text-to-speech has shown
much progress. However, previous methods utilize emotion encoders with emotion labels or leverage reference audio to extract emotion. In this paper, we propose manipulation of style
representation using vector arithmetic in latent style space for
emotion transfer. The advantage of this model is that even without explicitly encoded emotional information or reference audio, it successfully generates emotional speech with strength
control. By utilizing a Suppor Vector Machine (SVM) classifier and a style encoder architecture that is designed to extract
semantically meaningful style information, even unseen emotions for a speaker can be transferred by manipulation of its
style vector. Experiments show that the proposed method effectively transfer emotion, along with providing functionality for
controlling emotion strength.

### Emotional Speech Synthesis on Unseen Speakers

#### Korean

| Emotion     | Proposed    | Style Mean    |
|   :----:    |    :----:   |     :----:    |
| Neutral     | <audio controls><source src='./assets/kor_f_unseen.wav'></audio> |
| Angry       | <audio controls><source src='./assets/kor_f_unseen_angry20.wav'></audio> | <audio controls><source src='./assets/kor_f_unseen_angry_gstmean.wav'></audio>  |
| Sad         | <audio controls><source src='./assets/kor_f_unseen_sad20.wav'></audio> | <audio controls><source src='./assets/kor_f_unseen_sad_gstmean.wav'></audio>  |
| Happy       | <audio controls><source src='./assets/kor_f_unseen_happy20.wav'></audio> | <audio controls><source src='./assets/kor_f_unseen_happy_gstmean.wav'></audio>  |

#### English

| Emotion     | Proposed    | Style Mean    |
|   :----:    |    :----:   |     :----:    |
| Neutral     | <audio controls><source src='./assets/eng_f_unseen2.wav'></audio> |
| Angry       | <audio controls><source src='./assets/eng_f_unseen2_angry.wav'></audio> | <audio controls><source src='./assets/eng_f_unseen2_angry_gstmean.wav'></audio>  |
| Sad         | <audio controls><source src='./assets/eng_f_unseen2_sad.wav'></audio> | <audio controls><source src='./assets/eng_f_unseen2_sad_gstmean.wav'></audio>  |
| Happy       | <audio controls><source src='./assets/eng_f_unseen2_happy.wav'></audio> | <audio controls><source src='./assets/eng_f_unseen2_happy_gstmean.wav'></audio>  |
| Surprise    | <audio controls><source src='./assets/eng_f_unseen2_surprise.wav'></audio> | <audio controls><source src='./assets/eng_f_unseen2_surprise_gstmean.wav'></audio>  |

### Emotional Speech Synthesis on Seen Speakers

#### Korean

| Emotion     | Proposed    | Style Mean    |
|   :----:    |    :----:   |     :----:    |
| Neutral     | <audio controls><source src='./assets/kor_m_seen.wav'></audio> |
| Angry       | <audio controls><source src='./assets/kor_m_seen_angry.wav'></audio> | <audio controls><source src='./assets/kor_m_seen_angry_gstmean.wav'></audio>  |
| Sad         | <audio controls><source src='./assets/kor_m_seen_sad.wav'></audio> | <audio controls><source src='./assets/kor_m_seen_sad_gstmean.wav'></audio>  |
| Happy       | <audio controls><source src='./assets/kor_m_seen_happy.wav'></audio> | <audio controls><source src='./assets/kor_m_seen_happy_gstmean.wav'></audio>  |

#### English

| Emotion     | Proposed    | Style Mean    |
|   :----:    |    :----:   |     :----:    |
| Neutral     | <audio controls><source src='./assets/eng_f_seen.wav'></audio> |
| Angry       | <audio controls><source src='./assets/eng_f_seen_angry15.wav'></audio> | <audio controls><source src='./assets/eng_f_seen_angry_gstmean.wav'></audio>  |
| Sad         | <audio controls><source src='./assets/eng_f_seen_sad15.wav'></audio> | <audio controls><source src='./assets/eng_f_seen_sad_gstmean.wav'></audio>  |
| Happy       | <audio controls><source src='./assets/eng_f_seen_happy15.wav'></audio> | <audio controls><source src='./assets/eng_f_seen_happy_gstmean.wav'></audio>  |
| Surprise    | <audio controls><source src='./assets/eng_f_seen_surprise15.wav'></audio> | <audio controls><source src='./assets/eng_f_seen_surprise_gstmean.wav'></audio>  |

### Controlling Emotion Strength

| Emotion     | alpha = 1.0    | alpha = 1.5 | alpha = 2.0 | alpha = 2.5 |
|   :----:    |    :----:   |     :----:    |     :----:    |     :----:    |
| Angry       | <audio controls><source src='./assets/kor_f_unseen_angry10.wav'></audio> | <audio controls><source src='./assets/kor_f_unseen_angry15.wav'></audio>  | <audio controls><source src='./assets/kor_f_unseen_angry20.wav'></audio>  | <audio controls><source src='./assets/kor_f_unseen_angry25.wav'></audio>  |
| Sad         | <audio controls><source src='./assets/kor_f_unseen_sad10.wav'></audio> | <audio controls><source src='./assets/kor_f_unseen_sad15.wav'></audio>  | <audio controls><source src='./assets/kor_f_unseen_sad20.wav'></audio>  | <audio controls><source src='./assets/kor_f_unseen_sad25.wav'></audio>  |
| Happy       | <audio controls><source src='./assets/kor_f_unseen_happy10.wav'></audio> | <audio controls><source src='./assets/kor_f_unseen_happy15.wav'></audio>  | <audio controls><source src='./assets/kor_f_unseen_happy20.wav'></audio>  | <audio controls><source src='./assets/kor_f_unseen_happy25.wav'></audio>  |
