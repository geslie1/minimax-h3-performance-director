# H3 人物表演示例

以下均为原创文字示例，未经 H3 生成验证。带素材的示例使用明确的教学素材设定；实际任务只能使用已提供的素材及其真实编号，不能把示例中的图、音频或外貌当作用户附件。

## 1. T2VA：八秒，克制不等于面部冻结

输入：两位成年同事在办公室，镜头只拍负责人。画外同事说“项目取消了”，负责人平稳回应“知道了，先把文件收好。”。8 秒固定近景，不哭，不颤抖，不加道具；全程成功保持镇定，只给最终正文。

导演要点：通知是刺激，维持秩序是目标，回应是选择。控制成功可以贯穿全场，不必用额外微表情泄露难过。画外同事先发声为 S1，负责人为 S2；嘴部允许随发音活动。

```text
integrated_multimodal_description: [Shot 1] Live-action, an eight-second static close-up of an adult project lead in an office, facing a colleague just outside the frame. Her expression is composed throughout; her facial identity stays consistent while her lips and jaw move naturally when speaking. During the first two seconds, the off-screen adult colleague with a clear, level voice (S1) says: <d>[Chinese] 项目取消了</d> The lead listens without interrupting or revealing distress. After the statement ends, the lead with a steady, low voice (S2) replies at a natural pace: <d>[Chinese] 知道了，先把文件收好。</d> Her reply occupies approximately seconds two through six. During the remaining two seconds, her lips return to a relaxed resting position and she continues attending to the colleague. There are no tears, tremors, added props, or cuts.

overall_soundscape: Low office room tone remains consistent beneath the exchange.

non_diegetic_music: N/A
```

校核：第一句约 5 音节，后一句约 9 音节，分别安排约 2 秒和 4 秒；结尾 2 秒继续倾听。无台词跨切镜，无需额外连续标记。两句中文及原有标点保留，语气在标签外。

## 2. FL2VA：起止帧之间完成同一个动作

教学素材设定：Picture 1 是成年演员站在窗边的实际首帧，双手在胸前拿着已打开的单张卡片，目光落在卡片上、嘴角放松；Picture 2 是相同衣装、站位、光线与固定近景的尾帧，卡片和手的位置不变，演员抬眼看向画外来人，已露出自然微笑。目标 6 秒，无对白，无配乐，一镜到底。

```text
How the reference pictures align with the target video — Picture 1 (from Shot 1) aligns with the 0.00-second mark of the target video; Picture 2 (from Shot 1) aligns with the 6.00-second mark of the target video.

integrated_multimodal_description: [Shot 1] Live-action, a single six-second static close-up begins from the adult performer, framing, clothing, window light, hand positions, and open card shown in Picture 1. The performer finishes looking at the card during the first two seconds, and a small smile begins to form. Keeping the card and both hands at the same height, the performer then raises their gaze toward the person outside the frame. The smile develops openly rather than being suppressed. During the final two seconds, the gaze and smile settle into the precise ending state and composition established by Picture 2. No one speaks, and the camera remains still.

overall_soundscape: Quiet interior ambience continues throughout the shot.

non_diegetic_music: N/A
```

校核：首帧已持卡，不凭空加入接过或拆开卡片；结尾落点是抬眼微笑，不再加点头、转身或拥抱。最终画面到达 6.00 秒，起落由同一镜头完成。

## 3. Ref2VA：角色参考与音色参考分开管理

教学素材设定：Picture 1 仅提供成年女修复师的身份、短黑发和深绿色围裙；Picture 2 仅提供成年男同事的身份、短发和藏蓝工作衬衣；Audio 1 仅参考女修复师平稳、偏低的声线，不复制内容或整条音轨。两张图都不作为实际首帧。

目标：12 秒，档案室桌边两人面对一个未开的木箱。男同事手已搭在箱盖上，问“现在打开吗？”，她认出箱盖边缘的磨损圆形刻痕，回答“先别动，等我看清楚。”；他停手等候，箱子始终未开。不加回忆、悲伤或新台词，无配乐。6 秒处可切到她的反应。

```text
subject_definitions:
<Subject 1> is the adult female conservator from <Picture 1>, retaining her identity, short black hair, and dark green apron.
<Subject 2> is the adult male colleague from <Picture 2>, retaining his identity, short hair, and navy work shirt.
<Audio 1> is the voice-timbre reference for <Subject 1> (S2), providing a steady, low vocal quality without copied words or soundtrack.

summary:
[reference generation + audio reference] The twelve-second target video shows <Subject 1> and <Subject 2> beside a closed wooden crate. She notices a mark and asks him to wait. Their visual identities follow their respective references, while her newly performed dialogue uses the timbre of <Audio 1>.

retention_analysis:
<Subject 1> (appears in [Shot 1], [Shot 2]): fully_preserved - her defined identity, hair, and apron remain consistent through the new actions.
<Subject 2> (appears in [Shot 1]): fully_preserved - his defined identity, hair, and shirt remain consistent.
<Audio 1>: reference - its vocal timbre guides the conservator's new dialogue; its original signal and words are not copied.

detailed_description:
The target video is live-action with natural indoor light and restrained everyday performance. Facial features remain identifiable while allowing ordinary expression and speech movements.
[Shot 1] A static medium two-shot establishes an archive workroom and the closed wooden crate between the two colleagues. <Subject 1>, the conservator with short black hair and a dark green apron, stands at the left side of the table. <Subject 2>, the man with short hair and a navy work shirt, stands on the right, with his right hand already resting lightly on the lid and his other hand free. The tabletop supports the crate, and neither person lifts it. During the first two seconds, <Subject 2> (S1) asks in a clear conversational voice: <d>[Chinese] 现在打开吗？</d> He leaves the lid closed while waiting for her answer. <Subject 1> looks toward the worn circular mark on the near edge of the lid. Her attention settles there; she leans slightly closer without touching the box or displacing his hand. After his question ends, <Subject 1> (S2) uses the steady, low vocal timbre referenced from <Audio 1> and says: <d>[Chinese] 先别动，等我看清楚。</d> The line finishes before the sixth second. Her lips move freely with the words. He hears the request, lifts his right hand away from the lid, and lowers it beside his body. His empty hand remains lowered. The crate has not opened or changed position.
[Shot 2] At 00:06.000, the camera cuts to a static close-up of <Subject 1>, retaining her short black hair, apron neckline, and orientation toward the crate. The upper edge of the closed lid remains at the lower edge of the frame, keeping the object of her attention spatially clear. She continues examining the same mark rather than starting a new reaction. Her brow eases slightly as she obtains a clearer view, while her gaze stays directed downward. This change is small and continuous, with no tears, startle, or added memory sequence. The off-screen colleague waits and does not touch the crate again. During the final two seconds, she maintains this attentive position without speaking. The shot ends at twelve seconds with the lid still closed and the inspection unfinished.

overall_soundscape:
A low indoor ventilation hum continues throughout both shots. A brief light fabric rustle accompanies the man's withdrawing arm.

non_diegetic_music:
N/A
```

校核：两句约 5 与 8 音节，前 6 秒用于问答、看向刻痕与收手，后 6 秒只保留观察。Subject 编号不等于说话顺序：男同事先发声为 S1，女修复师为 S2。两张图仅定义角色，所以无需为 Picture 另起定义与保留条目。参考音色使用 `reference`，没有引入原音频台词或声称整轨复制；箱子未打开，符合指定切点。
