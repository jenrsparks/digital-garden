---
title: Categorization of Errors
source: original
category: Observability
---

_To Do_

### BaseException.java
```java
public class BaseException extends RuntimeException {
    private final String code;

    public BaseException(String message) {
        this(message, null, null);
    }

    public BaseException(String message, String code) {
        this(message, code, null);
    }

    public BaseException(String message, String code, Throwable cause) {
        super(message, cause);
        this.code = code;
    }

    public String getCode() {
        return code;
    }
}
```

### BusinessException.java
```java
public class BusinessException extends BaseException {
    public BusinessException(String message) {
        super(message);
    }

    public BusinessException(String message, String code) {
        super(message, code);
    }

    public BusinessException(String message, String code, Throwable cause) {
        super(message, code, cause);
    }
}
```

### ClientException.java
```java
public class ClientException extends BaseException {
    private final int httpStatus;

    public ClientException(String message, int httpStatus) {
        this(message, null, httpStatus, null);
    }

    public ClientException(String message, String code, int httpStatus) {
        this(message, code, httpStatus, null);
    }

    public ClientException(String message, String code, int httpStatus, Throwable cause) {
        super(message, code, cause);
        this.httpStatus = httpStatus;
    }

    public int getHttpStatus() {
        return httpStatus;
    }
}
```