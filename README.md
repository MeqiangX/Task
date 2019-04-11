# Task
定时任务相关

## SpringBoot 整合定时任务
1. 最简单的是直接用@Scheduled(cron表达式) 来运行
```java
/**
 * @description: 定时任务service
 * @author: Created by 云风 on 2019-04-11 11:27
 */
@Service
public class ScheduleService {

    @Scheduled(fixedRate = 5000)
    public void clearDataScheduleMethod(){
        System.out.println("现在时间：" + LocalDateTime.now() + " 定时任务启动.....");
    }

}

```
> 注意点是要在启动类上加上@EnableScheduling 注解来开启定时任务
