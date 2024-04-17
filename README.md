# if-else-recursion
// if else functions

// leap year
ALGORITHM LeapYearChecker
VAR
    year : INTEGER
BEGIN
    Read(year)
    IF (year % 4 = 0 AND NOT year % 100 = 0) OR (year % 400 = 0) THEN
        Write(year, " is a leap year.")
    ELSE
        Write(year, " is not a leap year.")
    END_IF
END

// ticket pricing
ALGORITHM TicketPricing
VAR
    age, ticketPrice : INTEGER
BEGIN
    Read(age)
    IF age <= 12 THEN
        ticketPrice := 10
    ELSE IF age >= 13 AND age <= 17 THEN
        ticketPrice := 15
    ELSE
        ticketPrice := 20
    END_IF
    
    Write("Your ticket price is $", ticketPrice)
END

// recursive functions

// fibonacci sequence
FUNCTION Fibonacci(n : INTEGER) : INTEGER
BEGIN
    IF n <= 1 THEN
        RETURN n
    ELSE
        RETURN Fibonacci(n-1) + Fibonacci(n-2)
    END_IF
END_FUNCTION

// power function
FUNCTION Power(num, n : INTEGER) : INTEGER
BEGIN
    IF n = 0 THEN
        RETURN 1
    ELSE IF n > 0 THEN
        RETURN num * Power(num, n - 1)
    END_IF
END_FUNCTION
