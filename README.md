# reverseaffinity-effects

Effects compositor — desmembrado do monorepo `reverseaffinity`.

## Estrutura
```
src/
├── python_ui/        # Interface Python (PyQt5)
│   ├── editor/       # Core editor engine
│   ├── reverseaffinity/  # App-specific modules
│   ├── tests/        # Test suite (pytest)
│   └── main.py       # Entry point
└── cpp_backend/      # C++ engine (performance-critical)
    ├── CMakeLists.txt
    ├── include/
    ├── src/
    └── test/
assets/               # Icons, resources
docs/                 # Documentation
```

## Executar (UI Python)
```bash
pip install -r src/python_ui/requirements.txt
python src/python_ui/main.py
```

## Compilar (C++ Backend)
```bash
cd src/cpp_backend
bash build.sh
```

## Testes
```bash
cd src/python_ui
QT_QPA_PLATFORM=offscreen python -m pytest tests/ -q
```

## Features
- Composição de efeitos
- Pipeline de filtros
- Keyframes e animação
