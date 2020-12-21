# Miro360:
.

The Windows version can be downloaded [here](https://drive.upm.es/index.php/s/l7bEnAcoC5lxvvo)


Miro360 is an interactive virtual reality tool for subjective assessment designed under the scope of ITU-T Study Group 12 and the Video Quality Experts Group in the development of the future ITU-T Recommendation P.360-VR for the subjective assessment of 360 videos using Head-Mounted Displays (HMDs).

The tool has been designed under the Unity3D engine to be used on multiple HMDs. Furthermore, it can be configured for a variety of custom or predefined questions while the video sequence is played and/or after its ending. 

The head tracking is also registered in degrees. The voting method is gaze-based using joysticks keys for confirmation.

# Citation:
If you use this software in your research, please cite the 
following article:
```
@INPROCEEDINGS{8966170,
  author={C. {Cortés} and P. {Pérez} and N. {García}},
  booktitle={2019 IEEE 9th International Conference on Consumer Electronics (ICCE-Berlin)}, 
  title={Unity3D-based app for 360VR subjective quality assessment with customizable questionnaires}, 
  year={2019},
  volume={},
  number={},
  pages={281-282},
  doi={10.1109/ICCE-Berlin47944.2019.8966170}}
```
# Playlist file configuration

```
"uri": "string"// 	Unique identifier of the sequence's video. The 
			identifier must be a string type with the absolute path of the 
			sequence's video 

"reference" : ["string"], //	Unique identifier of the sequence's reference, The identifier must 
		   	   	be a string type with the absolute path of the sequence's reference 


"src_id": "string" ,// 	String that identifies the content. This field is 
			key for the randomization because two consecutive "src_id" must not 
			be equal. 

"start": 0,// Integer for the starting second of the video. 

"duration": 20,// Integer for the duration of the video in seconds. 

"audio" : "string"
			String for disabling the audio. Different 
			string than "no" enables the audio. 

"post_sequence_timeout" : 5,//	Timeout for the votation, if the 
				field is not defined the time for voting will be infinite. 


"post_seq_questions": ["string"] // 	Field to show test(s) after the sequence, if 
				 	dcr is set, then it will be necessary to include the field 


Example of a complete sequence without audio and dcr post sequence question.

"uri": 
"E:/VQEG/Concert_3840x1920_25/Concert_3840x1920_25_QP_32.mp4", 
"reference" : 
["E:/VQEG/Concert_3840x1920_25/Concert_3840x1920_25_QP_15.mp4"], 
"src_id": "concert", 
"start": 0, 
"duration": 20, 
"audio" : "no", 
"post_sequence_timeout" : 5, 
"post_seq_questions": [ 
"dcr" 
] 
```
# Instructions:
  - The file miro360.json file must be located in the Miro360_Data folder (Example file is provided)

  - The generated reports will be located at the same folder with the name format: Result_YYYYMMDDHHMMSS.txt

  - Further information about miro360.json/report file format: https://github.com/zerepolbap/miro360


  - For HTC Vive: (Pro/Standard): 
    - The selection button is the touchpad button
    - For increasing the score in SSCQE use the touchpad (without pressing)

