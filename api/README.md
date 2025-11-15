## API Documentation

### Endpoints
- `POST /analyze` — анализ документа.  
  Параметры:  
  - `file` (PDF/DOCX/TXT).  
  - `features` (список: `ocr`, `notary_check`, `erp_sync`).  

- `GET /status` — проверка статуса лицензии.  

### Авторизация
- Заголовок: `X-License-Key: ВАШ_КЛЮЧ`.  
- Ошибка 403: лицензия недействительна.  

### Примеры
```bash
curl -X POST https://api.yoursite.com/analyze \
  -H "X-License-Key: abc123" \
  -F "file=@договор.pdf" \
  -F "features=ocr,notary_check"
