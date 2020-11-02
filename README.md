# Retry-Java-Example

### Retry with Wile loop

    public static void main(String[] args) {
        retryWithWileLoop();
    }
	
    public static void doSomething(int retry) {
        if (retry != 1) {
            throw new NullPointerException();
        }
    }
	
    public static void retryWithWileLoop() {
        int maxRetry = 3;
        int retry = 0;

        while (retry < maxRetry) {
            try {
                System.out.println("Retry : " + retry);
                doSomething(retry);
                break;
            } catch (Exception exception) {
                retry++;
            }
        }
    }

### Retry with For loop

### Retry with Recusive function

### Retry with Spring-Retry

### Retry with Retry Pattern
