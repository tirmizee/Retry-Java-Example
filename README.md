# Retry-Java-Example

    public static void main(String[] args) {
        retryWithWileLoop();
    }
	
    public static void doSomething(int retry) {
        if (retry != 1) {
            throw new NullPointerException();
        }
    }

### Retry with Wile-loop
	
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

### Retry with For-loop

	public static void retryWithForLoop() {

	    int maxRetry = 3;

	    for (int i = 0; i < maxRetry; i++) {
		try {
		    System.out.println("Retry : " + i);
		    doSomething(i);
		    break;
		} catch (Exception exception) {}
	    }

	}

### Retry with Recusive function

### Retry with Spring-Retry

### Retry with Retry-Pattern
