var
  IsPrime: array of Boolean; // признак, простое ли это число (для индекса массива)
  PrimeCandidate: Integer;   // кандидат в простое число
  Factor: Integer;           // исходное число для проверки 
begin
  SetLength(IsPrime, AMaxPrimes + 1);
 
  // Числа 0 и 1 - не простые (по определению)
  IsPrime[0] := False;
  IsPrime[1] := False;
 
  // Все числа от 2 до AMaxPrimes изначально простые
  for PrimeCandidate := 2 to AMaxPrimes do
    IsPrime[PrimeCandidate] := True;
 
  // Для каждого числа от 2 до AMaxPrimes:
  for Factor := 2 to AMaxPrimes do
  begin
    // Вычеркнуть все числа, делящиеся на это число
  end;
 
  // Выписать все не вычеркнутые числа
end;

var
  IsPrime: array of Boolean; // признак, простое ли это число (для индекса массива)
  PrimeCandidate: Integer;   // кандидат в простое число
  Factor: Integer;           // исходное число для проверки 
  FactorableNumber: Integer; // кратное число для вычёркивания
begin
  SetLength(IsPrime, AMaxPrimes + 1);
 
  // Числа 0 и 1 - не простые (по определению)
  IsPrime[0] := False;
  IsPrime[1] := False;
 
  // Все числа от 2 до AMaxPrimes изначально простые
  for PrimeCandidate := 2 to AMaxPrimes do
    IsPrime[PrimeCandidate] := True;
 
  // Для каждого числа от 2 до AMaxPrimes:
  for Factor := 2 to AMaxPrimes do
  begin
    // Вычеркнуть все числа, делящиеся на это число
    FactorableNumber := Factor + Factor;
    while FactorableNumber <= AMaxPrimes do
    begin
      IsPrime[FactorableNumber] := False;
      FactorableNumber := FactorableNumber + Factor;
    end;
  end;
 
  // Выписать все не вычеркнутые числа
end;
