---
layout: post
title: CROSS-SPEAKER EMOTION TRANSFER BY MANIPULATING SPEECH STYLE LATENTS
date: 2022-10-25
---
## Abstract

In recent years, emotional text-to-speech has shown considerable progress. However, it requires a large amount of labeled data, which is not easily accessible. Even if it is possible to acquire an emotional speech dataset, there is still a limitation in controlling emotion intensity. In this work, we propose a novel method for cross-speaker emotion transfer and manipulation using vector arithmetic in latent style space. By leveraging only a few labeled samples, we generate emotional speech from reading-style speech without losing the speaker identity. Furthermore, emotion strength is readily controllable using a scalar value, providing an intuitive way for users to manipulate speech. Experimental results show the proposed method affords superior performance in terms of expressiveness, naturalness, and controllability, preserving speaker identity.

## Emotion transfer to a reading style speaker
Note that all target speakers below are emotion-neutral reading style speakers.
Along with reading style speakers, we trained our model with a variety of speaking styles such as animation dubbing, whispering or screaming which are atypical for TTS dataset.
Averaging style vectors (Style Mean) showed poor performance when trained with our data, often failing to maintain speaker identity, while it worked well in terms of speaker identity when trained with emotion-neutral datasets only.
Also, note that generated sentences below are not in the dataset, so contents of a ground truth audio file do not match with the generated file.

| Target Emotion  | Ground Truth    | Proposed    | Style Mean    |
|   :----:    |    :----:   |    :----:   |     :----:    |
| Neutral     | <audio controls style="width: 200px;"><source src='./assets/xtine.wav'></audio>| <audio controls style="width: 200px;"><source src='./assets/xtine_100shot_neutral.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/xtine_base_neutral.wav'></audio>  |
| Angry       || <audio controls style="width: 200px;"><source src='./assets/xtine_100shot_angry.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/xtine_base_angry.wav'></audio>  |
| Sad         || <audio controls style="width: 200px;"><source src='./assets/xtine_100shot_sad.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/xtine_base_sad.wav'></audio>  |
| Happy       || <audio controls style="width: 200px;"><source src='./assets/xtine_100shot_happy.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/xtine_base_happy.wav'></audio>  |


| Target Emotion | Ground Truth    |  Proposed    | Style Mean    |
|   :----:    |    :----:   |     :----:   |     :----:    |
| Neutral     |<audio controls style="width: 200px;"><source src='./assets/iyuno-ko-m1.wav'></audio>| <audio controls style="width: 200px;"><source src='./assets/iyuno-ko-m1_100shot_neutral.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/iyuno-ko-m1_base_neutral.wav'></audio> |
| Angry       || <audio controls style="width: 200px;"><source src='./assets/iyuno-ko-m1_100shot_angry.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/iyuno-ko-m1_base_angry.wav'></audio>  |
| Sad         || <audio controls style="width: 200px;"><source src='./assets/iyuno-ko-m1_100shot_sad.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/iyuno-ko-m1_base_sad.wav'></audio>  |
| Happy       || <audio controls style="width: 200px;"><source src='./assets/iyuno-ko-m1_100shot_happy.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/iyuno-ko-m1_base_happy.wav'></audio>  |

## One-shot emotion transfer

| Emotion     | Proposed    |
|   :----:    |    :----:   |
| Neutral     | <audio controls><source src='./assets/hamin_oneshot_neutral.wav'></audio> |
| Angry       | <audio controls><source src='./assets/hamin_oneshot_angry.wav'></audio> |
| Sad         | <audio controls><source src='./assets/hamin_oneshot_sad.wav'></audio> | 
| Happy       | <audio controls><source src='./assets/hamin_oneshot_happy.wav'></audio> |

## Controlling Emotion Strength

| Emotion | alpha = 0.0    | alpha = 0.5 | alpha = 1.0 | alpha = 1.5 | alpha = 2.0 | 
|   :----:    |    :----:   |     :----:    |     :----:    |     :----:    |      :----:    |
| Angry       | <audio controls style="width: 200px;"><source src='./assets/seungjun_angry0.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/seungjun_angry0.5.wav'></audio>  | <audio controls style="width: 200px;"><source src='./assets/seungjun_angry1.0.wav'></audio>  | <audio controls style="width: 200px;"><source src='./assets/seungjun_angry1.5.wav'></audio>  | <audio controls style="width: 200px;"><source src='./assets/seungjun_angry2.0.wav'></audio>  | 
| Sad         | <audio controls style="width: 200px;"><source src='./assets/xtine_sad0.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/xtine_sad0.5.wav'></audio>  | <audio controls style="width: 200px;"><source src='./assets/xtine_sad1.0.wav'></audio>  | <audio controls style="width: 200px;"><source src='./assets/xtine_sad1.5.wav'></audio>  | <audio controls style="width: 200px;"><source src='./assets/xtine_sad2.0.wav'></audio>  |
| Happy       | <audio controls style="width: 200px;"><source src='./assets/ntis-eng_F_happy0.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/ntis-eng_F_happy0.5.wav'></audio>  | <audio controls style="width: 200px;"><source src='./assets/ntis-eng_F_happy1.0.wav'></audio>  | <audio controls style="width: 200px;"><source src='./assets/ntis-eng_F_happy1.5.wav'></audio>  | <audio controls style="width: 200px;"><source src='./assets/ntis-eng_F_happy2.0.wav'></audio>  |

## Ablation Study

| Emotion     | Proposed    | w/o Adv. spkr cls | w/o Cycle-consisency loss |
|   :----:    |    :----:   |    :----:   |     :----:   |
| Neutral     | <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_prop_neutral.wav'></audio> | <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_abl1_neutral.wav'></audio> |  <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_abl2_neutral.wav'></audio> |
| Angry       | <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_prop_angry.wav'></audio> |  <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_abl1_angry.wav'></audio> |  <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_abl2_angry.wav'></audio> | 
| Sad         | <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_prop_sad.wav'></audio> |  <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_abl1_sad.wav'></audio> |  <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_abl2_sad.wav'></audio> | 
| Happy       | <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_prop_happy.wav'></audio> |  <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_abl1_happy.wav'></audio> |  <audio controls style="width: 200px;"><source src='./assets/nts-eng_M_abl2_happy.wav'></audio> | 
