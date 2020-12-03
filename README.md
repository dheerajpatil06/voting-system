# voting-system
nominee1= input("enter the 1st nominee")
nominee2= input("enter the 2nd nominee")
nom_1_vote=0
nom_2_vote=0
voter_id=[1,2,3,4,5,6,7,8,9,10]
no_of_voter=len(voter_id)
while True:
    if voter_id==[]:
        print("voting session is over")
        if nom_1_vote>nom_2_vote:
            percent=(nom_1_vote/no_of_voter)
            print(nominee1,"has won" "with", percent,"% votes"  )
            break
        elif nom_2_vote>nom_1_vote:
            percent=(nom_2_vote/no_of_voter)
            print(nominee2,"has won" "with", percent,"% votes"  )
            break
    else:

        voter=int(input("enter the voter id:"))
        if voter in voter_id:
            print("you are voter")
            voter_id.remove(voter)
            vote=int(input("enter your vote to 1 or 2"))
            if vote==1:
                nom_1_vote+=1
                print("thank you for your vote")
            elif vote==2:
                nom_2_vote+=1
                print("thank you for your vote")
        else:
            print("you are not voter or already voted")

