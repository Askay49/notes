
Перечисление (enum) - это отдельный тип данных, задающий набор всех возможных целочисленных значений переменной этого типа.

### Объявление перечисления

```c
typedef enum
{
	OK = 0,
	SIZE_ERROR, // = 1
	CMD_ERROR, // = 2
	CRC_ERROR, // = 3
	//...
}error_t;
```

### Инициализация

```c
error_t error;
```

## Использование

```c
error_t handler(...)
{
	if(crc_check!= crc_calculate(buf,size))
	{
		return CRC_ERROR;
	}
	
	return OK;
}
