import cv2
cap=cv2.VideoCapture(0)
eye=cv2.CascadeClassifier(cv2.data.haarcascades+'haarcascade_eye.xml')
while True:
    ret,frame=cap.read()
    gray=cv2.cvtColor(frame , cv2.COLOR_BGR2RGB)
    eyes=eye.detectMultiScale(gray)
    for (x , y , w , h) in eyes:
        cv2.rectangle(frame , (x,y) , (x+w , y+h) , (0 , 0 , 255) , 4)
        cx=x+w//2
        cy=y+h//2
        cv2.circle(frame , (cx , cy) , 10 , (0 , 254 , 0) , -1)
        cv2.imshow('web' , frame)
    if cv2.waitKey(1) & 0XFF == ord ('q'):
            break
cap.release()
cv2.destroyAllWindows()
