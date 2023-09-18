---
title: 在複雜環境中偵測參與度並建立人機互動 / 呂昕儒 = Implementation of pre-engagement detection on human-robot interaction in complex environments / Sin-Ru Lu
authors: 昕儒. 呂
year: 2020
DOI: 
---
[Last_modified : : `$= dv.current().file.mtime`.]
### 文獻歸納
[Domain:: social_robot]
1. #framwork #implementation
2. [是否為交互合作::
	 否], 討論 robot 的 proactive 或 engagement
1. [如何整合各model:: Engagement 合併 NLP 判斷是否engaged，robot測試人類intention]
   ![[20230316_164709.jpg]]
2. [used__model:: intention model
				engagement model
				interaction model
				]
5. [Data__資料性質:: 語音, gaze, 表情]
6. [Algorithm :: 提升engagement的評估] #Conv+ #LSTM, #Two-stream, #3Dconv, #HMM, #fast_slow
8. [Equation :: engagement comfort index, naturalness index]