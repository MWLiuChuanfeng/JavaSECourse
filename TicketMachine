import java.util.Scanner;

public class TicketCmd {
    public static void main(String[] args){
        TicketMachine tm = new TicketMachine(3);
        System.out.println("今日收入：" + tm.getTotal() + "元");
        tm.resetSystem();
    }
}

class TicketMachine{
    private int price;
    private int balance;
    private int total;

    TicketMachine(int price){
        this.price = price;
        while (true){
        System.out.println("======欢迎使用自动售票机=======");
        System.out.println("本机销售固定票价" + price + "元的车票");
        System.out.println("请选择服务...");
        System.out.println("1、投币");
        System.out.println("2、打印车票");
        System.out.println("3、找零");
        System.out.println("4、退出");
        Scanner sc = new Scanner(System.in);
        int modeNumber = sc.nextInt();
        if (modeNumber == 4) {
            break;
        }
        switch (modeNumber){
            case 1:
                System.out.println("请输入投币金额：");
                balance = sc.nextInt();
                break;
            case 2:
                printTicket();
                break;
            case 3:
                System.out.println("找零：" + balance + "元");
                break;
            default:
                System.out.println("请输入正确的数字！");
        }
        }
    }

    void printTicket(){
        if(balance >= price){
            System.out.println("===================");
            System.out.println("This is a ticket");
            System.out.println("price :" + price + "元");
            System.out.println("===================");
            balance -= price;
            total += price;
            System.out.println("当前余额：" + balance + "元");
        }else {
            System.out.println("余额不足，请投币！");
        }
    }

    int getTotal(){
        return total;
    }

    void resetSystem(){
        price = 0;
        total = 0;
        balance = 0;
        System.out.println("系统已重置");
    }

}
