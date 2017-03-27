# Android-Ask-Yourself
记录学习过程中的问题，并尝试解答。  
1.[ThreadPoolExecutor](https://github.com/SDonGit/Android-Ask-Yourself/wiki/ThreadPoolExecutor)  
2.AsyncTask和Thread创建异步任务的区别？  
AsyncTask是串行执行的；Thread是并行执行的：  
When first introduced, AsyncTasks were executed serially on a single background  
thread. Starting with android.os.Build.VERSION_CODES#DONUT, this was changed  
to a pool of threads allowing multiple tasks to operate in parallel. Starting with  
android.os.Build.VERSION_CODES#HONEYCOMB, tasks are executed on a single  
thread to avoid common application errors caused by parallel execution.If you truly  
want parallel execution, you can invoke executeOnExecutor(java.util.concurrent.Executor,  
Object[]) with THREAD_POOL_EXECUTOR.  
![AysncTask_SerialExecutor](https://github.com/SDonGit/Android-Ask-Yourself/blob/master/AysncTask_SerialExecutor.png)
