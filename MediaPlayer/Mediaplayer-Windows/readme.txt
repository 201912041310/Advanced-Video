agora_demo_qt ������Ŀ
ע����Ҫvisual studio 2015�Ļ�������  ����Ҫ�����agora �Ĺ������ض�Ӧ��windows sdk �ļ�
Agora_native_sdk/dll �õ���dll���ļ�
Agora_native_sdk/include   ͷ�ļ�
Agora_native_sdk/lib    ���ӿ��ļ�
Agora_native_sdk/videokit ������Ƶ���ŵ��Ž��ļ�


ע��:
��Ƶ�����ļ�����ؽӿ� ֻ��Ҫ����videokit.h ͷ�ļ��µĽӿھ�����
��صĽӿ����£�
//��Ҫע��videoplaykit������    
void CreateVideoPlayerKitWithRtcEngine(agora::rtc::IRtcEngine *rtcEngine, int sampleRate);    
//���ýӿڻص� 
void setHandler(VideoPlayerKitEventHandler *handler);    
//����Ҫ���ŵ��ļ�    
void loadVideo(char * str,bool isAutoPlay);    
//��ȡ��ǰ�ļ����ŵĽ���    
long getCurrentPosition();    
//��ת����Ƶ�ļ����ŵ�λ��    
void seekTo(int msec);    
//��ͷ��ʼ    
void play();    
//��ͣ����    
void pause();    
//�ָ�����    
void resume();    
//�˳���Ƶ����    
void unload();    
//�Ƿ������˷����������    
void setAudioMixing(bool isAudioMix);
//����
void publish();
//������
void unPublish();

��صĵ���ʾ�����Բο�Demo�е�QTVideKit.cpp �ļ������ʵ��

����ע��һ�� QT�������������
SOURCES +=   
          #����videokit�ļ����µ�cpp�ļ�    
          $$PWD/Agora_native_sdk/videokit/ExtendAudioFrameObserver.cpp \    
          $$PWD/Agora_native_sdk/videokit/videoinfocallback.cpp \    
          $$PWD/Agora_native_sdk/videokit/videokit.cpp
          $$PWD/Agora_native_sdk/videokit/ZD3DRender.cpp


  


#���ͷ�ļ�
INCLUDEPATH += $$PWD/Agora_native_sdk/include \               
                        $$PWD/Agora_native_sdk/videokit

#��Ӹ��ӿ��ļ� 
win32: LIBS += -L$$PWD/Agora_native_sdk/lib/ -lagora_rtc_sdk -lre_sampler -lVideoPlayerKit

