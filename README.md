# Step-1

변수 입력을 받아라

    word,num,way = input().split()
    num = int(num)

    word_list = []
    for i in range(len(word)):
      word_list.append(word[i])


왼쪽으로 입력받은 num만큼 shift하라

    if (way =='l'or way=='L') :
       if(num>=0):
         for i in range(num):
            temp = word_list[0]

            for i in range(1,len(word_list)):
              word_list[i-1] = word_list[i]


            word_list[len(word_list)-1] = temp
         result = "".join(word_list)

       else:
         for i in range(abs(num)):
           temp = word_list[len(word_list)-1]
           print(temp)
           for j in range(len(word_list)-1,0,-1):
             word_list[j] = word_list[j-1]

           word_list[0]=temp
         result = "".join(word_list)
     
     
오른쪽으로 입력받은 num만큼 shift하라

    else:
      if(num>=0):
        for i in range(abs(num)):
           temp = word_list[len(word_list)-1]

           for i in range(len(word_list)-1,0,-1):
             word_list[i] = word_list[i-1]

           word_list[0]=temp
        result = "".join(word_list)

      else:
        for i in range(abs(num)):
            temp = word_list[0]

            for i in range(1,len(word_list)):
              word_list[i-1] = word_list[i]


            word_list[len(word_list)-1] = temp

결과를 출력하라

        print(result)
