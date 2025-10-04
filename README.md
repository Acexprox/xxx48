# الأسطورة أونلاين (USO Online)

Arabic e-payment and online services platform built with Next.js and FastAPI.

## Project Structure

- **Backend**: FastAPI application with MongoDB integration
  - Port: 8001
  - API Prefix: `/api`
  - Location: `/app/backend/`

- **Frontend**: Next.js 14 application with App Router
  - Port: 3000
  - Location: `/app/frontend/`
  
- **Database**: MongoDB (running on port 27017)

## Services

All services are managed by supervisor:

```bash
# Check status
sudo supervisorctl status

# Restart services
sudo supervisorctl restart backend
sudo supervisorctl restart frontend
sudo supervisorctl restart mongodb
sudo supervisorctl restart all
```

## API Endpoints

- `GET /api/` - Hello World endpoint
- `POST /api/status` - Create status check
- `GET /api/status` - Get all status checks

## Environment Variables

### Backend (.env)
- `MONGO_URL=mongodb://localhost:27017`
- `DB_NAME=myapp_db`
- `CORS_ORIGINS=*`

### Frontend (.env)
- `REACT_APP_BACKEND_URL=http://localhost:8001`

## Development

Backend and frontend have hot-reload enabled. Only restart services when:
- Installing new dependencies
- Modifying .env files

## Features

This is a full-featured Arabic e-payment platform with:
- Online payment services
- Mobile recharge
- Gaming services
- Digital cards
- Multiple payment methods
