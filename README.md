// 자판기 프로그램 [공대밥판기(공대생들을 위한 밥판기)]
// 대구가톨릭대학교 공대생들을 위한 도시락 자판기
// 만들게 된 계기 : 공대생들은 공강 시간에 식사를 하러 가기에 식당과 편의점이 너무나도 멀다.
// 시간이 촉박한 학생들을 위해 도시락 자판기가 출시가 된다면 시간도 절약하고 편리하고 간편하게 먹을 수 있을 것이다.
// 음식 메뉴 : 스팸마요(3600), 치킨마요(3000), 돈치마요(3600), 김치볶음밥(3900), 참치마요(3000)
//           치즈불닭(5500), 소불고기덮밥(4200)
#include <stdio.h>
#include <stdlib.h>
// 메뉴의 가격을 지정
#define Spam 3600
#define Chicken 3000
#define BeefChicken 3600
#define Gimchi 3900
#define Tuna 3000
#define CheeseFire 5500
#define Bulgogi 4200

int MenuChoice = 0; // 메뉴 선택
int Money = 0;  // 투입된 돈
int Number = 0; // 품목갯수
int Total = 0;  // 품목갯수와 투입된 돈의 총합
int Rest = 0;   // 투입된 돈에서 돈의 총합을 뺀 나머지

char YorN = { 0 };  // Y와 N의 입력을 받기 위한 함수
int MainMenu() {
    while(1) {
        printf("최소 투입금액은 3,000원입니다.\n");    // 가장 낮은 메뉴의 가격 : 3,000원
        printf("금액을 입력해주세요 >>> ");
        scanf("%d", &Money);    // 사용자로부터 금액을 입력 받음
        
        if(Money<3000) {        // 입력받은 금액이 3,000원 보다 적거나 6,000원 보다 많을시
            printf("금액이 너무 적습니다.\n\n");
            continue;                           // 다시 처음으로 돌아가 입력을 받음
        }
        else {
            printf("%d원 투입되었습니다.\n\n", Money);    // 투입된 금액을 확인시켜주는 과정
            return 0;
        }
    }
}

int Menu() {
    while(1) {
        printf(" -------공대밥판기---------\n");
        printf(" ∙   1. 스팸마요(3,600원)\n");   // 1번 메뉴
        printf(" ∙   2. 치킨마요(3,000원)\n");   // 2번 메뉴
        printf(" ∙   3. 돈치마요(3,600원)\n");   // 3번 메뉴
        printf(" ∙   4. 김치볶음밥(3,900원)\n");  // 4번 메뉴
        printf(" ∙   5. 참치마요(3,000원)\n");   // 5번 메뉴
        printf(" ∙   6. 치즈불닭(5,500원)\n");   // 6번 메뉴
        printf(" ∙   7. 불고기덮밥(4,200원)\n");  // 7번 메뉴
        printf(" -----------------------\n\n");
        
        printf("드시고 싶은 음식을 번호로 입력해주세요 >>> ");
        scanf("%d", &MenuChoice);
        
        if((MenuChoice<1) || (MenuChoice>7)) {      // 1~7번 사이의 메뉴가 아닐시
            printf("\n잘못 입력하셨습니다.\n");
            printf("다시 한 번 입력해주세요.\n\n");
            continue;
        }
        fflush(stdin);      // 저장된 버퍼를 없애기
        
        switch(MenuChoice) {            // 1번부터 7번까지의 메뉴별 설명
            case 1 :
                printf("스팸마요를 선택하셨습니다.\n");
                printf("원하는 갯수를 입력해주세요 >>> ");
                scanf("%d", &Number);
                printf("\n");
                if(Number<1) {
                    printf("잘못된 갯수입니다.\n");
                    printf("다시 한 번 입력해주세요.\n\n");
                    continue;
                }
                break;
            case 2:
                printf("치킨마요를 선택하셨습니다.\n");
                printf("원하는 갯수를 입력해주세요 >>> ");
                scanf("%d", &Number);
                printf("\n");
                if(Number<1) {
                    printf("잘못된 갯수입니다.\n");
                    printf("다시 한 번 입력해주세요.\n\n");
                    continue;
                }
                break;
            case 3:
                printf("돈치마요를 선택하셨습니다.\n");
                printf("원하는 갯수를 입력해주세요 >>> ");
                scanf("%d", &Number);
                printf("\n");
                if(Number<1) {
                    printf("잘못된 갯수입니다.\n");
                    printf("다시 한 번 입력해주세요.\n\n");
                    continue;
                }
                break;
            case 4:
                printf("김치볶음밥을 선택하셨습니다.\n");
                printf("원하는 갯수를 입력해주세요 >>> ");
                scanf("%d", &Number);
                printf("\n");
                if(Number<1) {
                    printf("잘못된 갯수입니다.\n");
                    printf("다시 한 번 입력해주세요.\n\n");
                    continue;
                }
                break;
            case 5:
                printf("참치마요를 선택하셨습니다.\n");
                printf("원하는 갯수를 입력해주세요 >>> ");
                scanf("%d", &Number);
                printf("\n");
                if(Number<1) {
                    printf("잘못된 갯수입니다.\n");
                    printf("다시 한 번 입력해주세요.\n\n");
                    continue;
                }
                break;
            case 6:
                printf("치즈불닭을 선택하셨습니다.\n");
                printf("원하는 갯수를 입력해주세요 >>> ");
                scanf("%d", &Number);
                printf("\n");
                if(Number<1) {
                    printf("잘못된 갯수입니다.\n");
                    printf("다시 한 번 입력해주세요.\n\n");
                    continue;
                }
                break;
            case 7:
                printf("불고기덮밥을 선택하셨습니다.\n");
                printf("원하는 갯수를 입력해주세요 >>> ");
                scanf("%d", &Number);
                printf("\n");
                if(Number<1) {
                    printf("잘못된 갯수입니다.\n");
                    printf("다시 한 번 입력해주세요.\n\n");
                    continue;
                }
                break;
                printf("\n");
        }
        switch(MenuChoice) {
            case 1:
                if((Spam*Number)>Money) {       // 구입금액보다 투입금액이 적을 때
                    printf("금액이 부족합니다.\n");
                    continue;
                }
                else {
                    Total = Spam*Number;
                    Rest = Money-Total;
                    Money = Rest;
                    printf("%d원을 사용하셨습니다.\n", Total);
                    printf("거스름돈은 %d원입니다.\n", Rest);
                }
                break;
            case 2:
                if((Chicken*Number)>Money) {
                    printf("금액이 부족합니다.\n");
                    continue;
                }
                else {
                    Total = Chicken*Number;
                    Rest = Money-Total;
                    Money = Rest;
                    printf("%d원을 사용하셨습니다.\n", Total);
                    printf("거스름돈은 %d원입니다.\n", Rest);
                }
                break;
            case 3:
                if((BeefChicken*Number)>Money) {
                    printf("금액이 부족합니다.\n");
                    continue;
                }
                else {
                    Total = BeefChicken*Number;
                    Rest = Money-Total;
                    Money = Rest;
                    printf("%d원을 사용하셨습니다.\n", Total);
                    printf("거스름돈은 %d원입니다.\n", Rest);
                }
                break;
            case 4:
                if((Gimchi*Number)>Money) {
                    printf("금액이 부족합니다.\n");
                    continue;
                }
                else {
                    Total = Gimchi*Number;
                    Rest = Money-Total;
                    Money = Rest;
                    printf("%d원을 사용하셨습니다.\n", Total);
                    printf("거스름돈은 %d원입니다.\n", Rest);
                }
                break;
            case 5:
                if((Tuna*Number)>Money) {
                    printf("금액이 부족합니다.\n");
                    continue;
                }
                else {
                    Total = Tuna*Number;
                    Rest = Money-Total;
                    Money = Rest;
                    printf("%d원을 사용하셨습니다.\n", Total);
                    printf("거스름돈은 %d원입니다.\n", Rest);
                }
                break;
            case 6:
                if((CheeseFire*Number)>Money) {
                    printf("금액이 부족합니다.\n");
                    continue;
                }
                else {
                    Total = CheeseFire*Number;
                    Rest = Money-Total;
                    Money = Rest;
                    printf("%d원을 사용하셨습니다.\n", Total);
                    printf("거스름돈은 %d원입니다.\n", Rest);
                }
                break;
            case 7:
                if((Bulgogi*Number)>Money) {
                    printf("금액이 부족합니다.\n");
                    continue;
                }
                else {
                    Total = Bulgogi*Number;
                    Rest = Money-Total;
                    Money = Rest;
                    printf("%d원을 사용하셨습니다.\n", Total);
                    printf("거스름돈은 %d원입니다.\n", Rest);
                }
                break;
        }
End :
        fflush(stdin);      // 저장된 버퍼 없애기
        printf("\n공대밥판기를 종료하시겠습니까?\n");
        printf("y(YES) 또는 n(NO)를 입력해주세요.\n");
        scanf("%c", &YorN);
        
        if(YorN == 'y') {
            printf("\n");
            printf("∙∙∙∙∙∙∙∙∙ 공대밥판기를 종료합니다 ∙∙∙∙∙∙∙∙∙\n");
            printf("   공대밥판기는 여러분의 앞날을 응원합니다!   \n");
            printf("   맛있는 식사되세요^_^                 \n");
            printf("∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙∙\n");
            break;
        }
        else if(YorN == 'n') {
            printf("\n공대밥판기를 계속 운영합니다.\n");
            continue;
        }
        else {
            printf("\n잘못 입력하셨습니다.\n");
            printf("y(YES) 또는 n(NO)로 다시 입력해주세요.\n");
            goto End;
        }
        
        
    }
    return 0;
}

int main(void) {
    MainMenu();
    Menu();
    return 0;
}
