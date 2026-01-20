# Resumen del proyecto WatermelonD

## Estructura del Proyecto

```
WatermelonD/
├── ROADMAP.md
├── walkthrough.md
├── README.md
├── install.sh
├── start.sh
├── resumen.md
├── NeoCore.py
├── source/
│   ├── conf.py
│   └── training_data/
├── resources/
│   ├── Blue/
│   │   ├── bro_bridge.py
│   │   ├── install_nb.sh
│   │   ├── README.md
│   │   ├── bro_agent.py
│   │   ├── test_simulation.py
│   │   ├── esp32_cam/
│   │   ├── MNB/
│   │   │   ├── README.md
│   │   │   ├── ESP32/
│   │   │   │   ├── main.py
│   │   │   │   └── boot.py
│   │   │   └── PiZero/
│   │   │       └── agent.py
│   │   └── experiments/
│   │       ├── whatsapp_to_json.py
│   │       ├── README.md
│   │       ├── ingest_conversations.py
│   │       ├── finetune_tio.py
│   │       ├── merge_lora.py
│   │       └── txt_to_json.py
│   ├── tests/
│   │   ├── test_sysadmin.py
│   │   ├── test_fuzzy_logic.py
│   │   ├── test_cortex.py
│   │   ├── test_brain.py
│   │   ├── test_sherlock.py
│   │   ├── test_knowledge_graph.py
│   │   ├── test_sentiment.py
│   │   ├── test_memory.py
│   │   ├── test_speaker_config.py
│   │   └── test_perf_cortex.py
│   └── tools/
│       ├── download_model.py
│       ├── test_conversation_flow.py
│       ├── download_vosk_model.py
│       ├── analyze_code.py
│       ├── check_neocore.py
│       ├── start_face.sh
│       ├── install_piper.py
│       ├── optimize_whisper.py
│       ├── train_chat.py
│       ├── seed_knowledge.py
│       ├── migrate_db.py
│       └── download_big_model.py
├── config/
├── modules/
│   ├── wifi_manager.py
│   ├── chat.py
│   ├── dashboard_data.py
│   ├── sherlock.py
│   ├── calendar.py
│   ├── web_admin.py
│   ├── cast_manager.py
│   ├── vision.py
│   ├── intent_manager.py
│   ├── file_manager.py
│   ├── utils.py
│   ├── config_manager.py
│   ├── sentiment.py
│   ├── reminders.py
│   ├── voice_manager.py
│   ├── ssh_manager.py
│   ├── ai_engine.py
│   ├── alarms.py
│   ├── guard.py
│   ├── database.py
│   ├── logger.py
│   ├── brain.py
│   ├── speaker.py
│   ├── network.py
│   ├── date_parser.py
│   ├── sysadmin.py
│   └── skills/
│       ├── __init__.py
│       ├── system.py
│       ├── ssh.py
│       ├── content.py
│       ├── time_date.py
│       ├── media.py
│       ├── organizer.py
│       ├── network.py
│       └── files.py
├── docs/
│   ├── whisper_manual.md
│   ├── atackdb.md
│   ├── changelog.md
│   ├── tio_personality.md
│   ├── install_fedora.md
│   ├── all.md
│   ├── train.md
│   ├── brain.md
│   ├── info.md
│   └── refactorizar.md
├── database/
│   └── init_db.py
└── web/
    └── static/
        ├── css/
        ├── js/
        └── templates/
```

## Estadísticas Generales

- **Total Líneas de Código:** 7217
- **Total Clases:** 39
- **Total Funciones:** 330
- **Total Asignaciones de Variables (Aprox):** 1542
- **Total TODOs/FIXMEs:** 1

## Dependencias (requirements.txt)

- python-vlc
- numpy
- vosk
- psutil
- pyaudio
- rapidfuzz
- scikit-learn
- dateparser
- flask
- paramiko
- cryptography
- flask-socketio
- eventlet
- face_recognition
- opencv-python
- llama-cpp-python
- huggingface-hub
- pychromecast

## Tareas Pendientes (TODOs/FIXMEs)

- [resources/tools/analyze_code.py] "todos": [line.strip() for line in lines if "# TODO" in line or "# FIXME" in line]

## Detalle por Archivo

### NeoCore.py

- **Líneas:** 486
- **Clases:** 1
  - `class NeoCore`
- **Funciones:** 18
  - `def __init__`
  - `def on_vision_event`
  - `def speak`
  - `def setup_vlc`
  - `def on_closing`
  - `def start_background_tasks`
  - `def on_voice_command`
  - `def handle_command`
  - `def handle_unrecognized_command`
  - `def process_event_queue`
  - `def proactive_update_loop`
  - `def _check_frequent_tasks`
  - `def check_calendar_events`
  - `def execute_action`
  - `def action_responder_simple`
  - `def action_consultar_citas`
  - `def give_morning_summary`
  - `def handle_learning_response`
- **Variables (Est.):** 105

---

### modules/database.py

- **Líneas:** 478
- **Clases:** 1
  - `class DatabaseManager`
- **Funciones:** 27
  - `def __init__`
  - `def get_connection`
  - `def init_db`
  - `def log_interaction`
  - `def get_recent_interactions`
  - `def add_fact`
  - `def get_fact`
  - `def search_facts`
  - `def add_alias`
  - `def get_alias`
  - `def get_all_aliases`
  - `def log_event`
  - `def get_recent_events`
  - `def search_memories`
  - `def update_concept`
  - `def get_concept`
  - `def get_top_concepts`
  - `def add_relation`
  - `def get_related_concepts`
  - `def get_path`
  - `def infer_problems`
  - `def log_surprise`
  - `def get_recent_surprises`
  - `def get_interactions_by_date`
  - `def add_daily_summary`
  - `def get_daily_summary`
  - `def close`
- **Variables (Est.):** 77

---

### modules/web_admin.py

- **Líneas:** 439
- **Clases:** 0
- **Funciones:** 38
  - `def login_required`
  - `def wrapped_view`
  - `def index`
  - `def login`
  - `def logout`
  - `def dashboard`
  - `def services`
  - `def network`
  - `def actions`
  - `def terminal`
  - `def logs`
  - `def speech`
  - `def settings`
  - `def ssh_page`
  - `def explorer`
  - `def knowledge`
  - `def face`
  - `def update_face`
  - `def restart_system`
  - `def api_stats`
  - `def api_logs`
  - `def api_speech_history`
  - `def api_services`
  - `def api_control_service`
  - `def api_network`
  - `def api_wifi_scan`
  - `def api_wifi_connect`
  - `def api_dashboard_data`
  - `def api_terminal`
  - `def api_terminal_complete`
  - `def api_actions`
  - `def api_ssh_list`
  - `def api_ssh_add`
  - `def api_ssh_delete`
  - `def api_files_list`
  - `def api_files_read`
  - `def api_files_save`
  - `def run_server`
- **Variables (Est.):** 103

---

### install.sh

- **Líneas:** 250
- **Clases:** 0
- **Funciones:** 0
- **Variables (Est.):** 29

---

### modules/sysadmin.py

- **Líneas:** 194
- **Clases:** 1
  - `class SysAdminManager`
- **Funciones:** 10
  - `def __init__`
  - `def get_cpu_temp`
  - `def get_disk_usage`
  - `def get_ram_usage`
  - `def get_full_status`
  - `def get_services`
  - `def control_service`
  - `def get_network_info`
  - `def run_command`
  - `def get_file_completions`
- **Variables (Est.):** 31

---

### modules/brain.py

- **Líneas:** 183
- **Clases:** 1
  - `class Brain`
- **Funciones:** 10
  - `def __init__`
  - `def set_ai_engine`
  - `def process_input`
  - `def learn_alias`
  - `def store_interaction`
  - `def get_last_context`
  - `def remember_event`
  - `def recall_events`
  - `def retrieve_context`
  - `def consolidate_memory`
- **Variables (Est.):** 27

---

### resources/tools/download_vosk_model.py

- **Líneas:** 180
- **Clases:** 0
- **Funciones:** 6
  - `def get_system_resources`
  - `def recommend_model`
  - `def download_file`
  - `def install_model`
  - `def update_config`
  - `def main`
- **Variables (Est.):** 37

---

### modules/date_parser.py

- **Líneas:** 172
- **Clases:** 0
- **Funciones:** 3
  - `def parse_reminder_from_text`
  - `def _parse_reminder_from_text_original`
  - `def parse_alarm_from_text`
- **Variables (Est.):** 52

---

### resources/tools/analyze_code.py

- **Líneas:** 167
- **Clases:** 0
- **Funciones:** 4
  - `def analyze_file`
  - `def get_project_tree`
  - `def get_requirements`
  - `def main`
- **Variables (Est.):** 69
- **TODOs:** 1

---

### modules/vision.py

- **Líneas:** 161
- **Clases:** 2
  - `class FaceDB`
  - `class VisionManager`
- **Funciones:** 10
  - `def __init__`
  - `def _load_db`
  - `def save_db`
  - `def add_face`
  - `def __init__`
  - `def start`
  - `def stop`
  - `def _detect_motion`
  - `def _loop`
  - `def _identify_user`
- **Variables (Est.):** 44

---

### modules/guard.py

- **Líneas:** 152
- **Clases:** 1
  - `class Guard`
- **Funciones:** 9
  - `def __init__`
  - `def load_signatures`
  - `def start`
  - `def stop`
  - `def monitor_loop`
  - `def check_log_signatures`
  - `def check_system_signatures`
  - `def register_event`
  - `def trigger_alert`
- **Variables (Est.):** 33

---

### resources/tools/optimize_whisper.py

- **Líneas:** 150
- **Clases:** 0
- **Funciones:** 4
  - `def check_dependencies`
  - `def benchmark_model`
  - `def main`
  - `def update_config`
- **Variables (Est.):** 34

---

### resources/NB/bro_agent.py

- **Líneas:** 149
- **Clases:** 1
  - `class BroAgent`
- **Funciones:** 8
  - `def __init__`
  - `def on_connect`
  - `def on_message`
  - `def handle_command`
  - `def perform_status_check`
  - `def speak`
  - `def proximity_loop`
  - `def run`
- **Variables (Est.):** 36

---

### modules/speaker.py

- **Líneas:** 145
- **Clases:** 1
  - `class Speaker`
- **Funciones:** 6
  - `def __init__`
  - `def _load_config`
  - `def _check_engine`
  - `def _process_queue`
  - `def speak`
  - `def is_busy`
- **Variables (Est.):** 38

---

### resources/tools/train_chat.py

- **Líneas:** 137
- **Clases:** 0
- **Funciones:** 3
  - `def init_db`
  - `def load_data`
  - `def train`
- **Variables (Est.):** 35

---

### modules/network.py

- **Líneas:** 131
- **Clases:** 1
  - `class NetworkManager`
- **Funciones:** 8
  - `def __init__`
  - `def check_dependencies`
  - `def run_command`
  - `def get_local_ip`
  - `def scan_network`
  - `def check_host`
  - `def whois_lookup`
  - `def analyze_security`
- **Variables (Est.):** 27

---

### modules/voice_manager.py

- **Líneas:** 122
- **Clases:** 1
  - `class VoiceManager`
- **Funciones:** 7
  - `def __init__`
  - `def setup_vosk`
  - `def get_grammar`
  - `def start_listening`
  - `def stop_listening`
  - `def set_processing`
  - `def _continuous_voice_listener`
- **Variables (Est.):** 34

---

### modules/ssh_manager.py

- **Líneas:** 119
- **Clases:** 1
  - `class SSHManager`
- **Funciones:** 9
  - `def __init__`
  - `def _load_servers`
  - `def _save_servers`
  - `def add_server`
  - `def remove_server`
  - `def connect`
  - `def execute`
  - `def disconnect`
  - `def get_servers_list`
- **Variables (Est.):** 20

---

### resources/tools/seed_knowledge.py

- **Líneas:** 112
- **Clases:** 0
- **Funciones:** 0
- **Variables (Est.):** 7

---

### resources/NB/bro_bridge.py

- **Líneas:** 110
- **Clases:** 1
  - `class BroBridge`
- **Funciones:** 9
  - `def __init__`
  - `def on_connect`
  - `def on_message`
  - `def handle_proximity`
  - `def handle_status`
  - `def check_theatrical_trigger`
  - `def start_conversation`
  - `def speak`
  - `def run`
- **Variables (Est.):** 27

---

### resources/experiments/finetune_tio.py

- **Líneas:** 110
- **Clases:** 0
- **Funciones:** 1
  - `def format_instruction`
- **Variables (Est.):** 52

---

### modules/dashboard_data.py

- **Líneas:** 99
- **Clases:** 1
  - `class DashboardDataManager`
- **Funciones:** 7
  - `def __init__`
  - `def get_weather`
  - `def _get_weather_desc`
  - `def get_news`
  - `def get_calendar_summary`
  - `def get_all_data`
  - `def get_calendar_summary_robust`
- **Variables (Est.):** 23

---

### modules/skills/organizer.py

- **Líneas:** 99
- **Clases:** 1
  - `class OrganizerSkill`
- **Funciones:** 7
  - `def crear_recordatorio_voz`
  - `def crear_alarma_voz`
  - `def consultar_recordatorios_dia`
  - `def consultar_alarmas`
  - `def iniciar_dialogo_temporizador`
  - `def consultar_temporizador`
  - `def crear_temporizador_directo`
- **Variables (Est.):** 27

---

### resources/NB/test_simulation.py

- **Líneas:** 96
- **Clases:** 0
- **Funciones:** 3
  - `def run_bridge`
  - `def run_agent`
  - `def test_scenario`
- **Variables (Est.):** 19

---

### resources/experiments/ingest_conversations.py

- **Líneas:** 91
- **Clases:** 0
- **Funciones:** 1
  - `def ingest_conversations`
- **Variables (Est.):** 21

---

### modules/skills/system.py

- **Líneas:** 91
- **Clases:** 1
  - `class SystemSkill`
- **Funciones:** 7
  - `def check_status`
  - `def apagar`
  - `def diagnostico`
  - `def queja_factura`
  - `def restart_service`
  - `def update_system`
  - `def find_file`
- **Variables (Est.):** 15

---

### modules/wifi_manager.py

- **Líneas:** 89
- **Clases:** 1
  - `class WifiManager`
- **Funciones:** 3
  - `def __init__`
  - `def scan`
  - `def connect`
- **Variables (Est.):** 15

---

### resources/tools/download_big_model.py

- **Líneas:** 87
- **Clases:** 0
- **Funciones:** 3
  - `def download_file`
  - `def install_model`
  - `def update_config`
- **Variables (Est.):** 23

---

### resources/NB/install_nb.sh

- **Líneas:** 86
- **Clases:** 0
- **Funciones:** 0
- **Variables (Est.):** 19

---

### modules/alarms.py

- **Líneas:** 85
- **Clases:** 1
  - `class AlarmManager`
- **Funciones:** 8
  - `def __init__`
  - `def _load_alarms`
  - `def _save_alarms`
  - `def add_alarm`
  - `def delete_alarm`
  - `def get_all_alarms`
  - `def get_alarms_summary`
  - `def check_alarms`
- **Variables (Est.):** 21

---

### modules/chat.py

- **Líneas:** 84
- **Clases:** 1
  - `class ChatManager`
- **Funciones:** 3
  - `def __init__`
  - `def get_response`
  - `def reset_context`
- **Variables (Est.):** 26

---

### modules/cast_manager.py

- **Líneas:** 83
- **Clases:** 1
  - `class CastManager`
- **Funciones:** 5
  - `def __init__`
  - `def start_discovery`
  - `def get_devices`
  - `def play_media`
  - `def stop_media`
- **Variables (Est.):** 11

---

### modules/file_manager.py

- **Líneas:** 83
- **Clases:** 1
  - `class FileManager`
- **Funciones:** 5
  - `def __init__`
  - `def list_directory`
  - `def read_file`
  - `def save_file`
  - `def search_files`
- **Variables (Est.):** 10

---

### modules/ai_engine.py

- **Líneas:** 82
- **Clases:** 1
  - `class GemmaEngine`
- **Funciones:** 3
  - `def __init__`
  - `def load_model`
  - `def generate_response`
- **Variables (Est.):** 28

---

### resources/tools/install_piper.py

- **Líneas:** 81
- **Clases:** 0
- **Funciones:** 3
  - `def download_file`
  - `def install_piper`
  - `def update_config`
- **Variables (Est.):** 21

---

### modules/sherlock.py

- **Líneas:** 81
- **Clases:** 1
  - `class Sherlock`
- **Funciones:** 3
  - `def __init__`
  - `def diagnose`
  - `def _run_command`
- **Variables (Est.):** 11

---

### modules/skills/media.py

- **Líneas:** 80
- **Clases:** 1
  - `class MediaSkill`
- **Funciones:** 3
  - `def controlar_radio`
  - `def cast_video`
  - `def stop_cast`
- **Variables (Est.):** 14

---

### modules/calendar.py

- **Líneas:** 76
- **Clases:** 1
  - `class CalendarManager`
- **Funciones:** 7
  - `def __init__`
  - `def _load_events`
  - `def _save_events`
  - `def add_event`
  - `def get_events_for_month`
  - `def get_events_for_day`
  - `def get_events_summary_for_day`
- **Variables (Est.):** 20

---

### resources/MNB/PiZero/agent.py

- **Líneas:** 75
- **Clases:** 0
- **Funciones:** 4
  - `def get_cpu_temp`
  - `def get_system_stats`
  - `def on_connect`
  - `def main`
- **Variables (Est.):** 10

---

### modules/skills/content.py

- **Líneas:** 75
- **Clases:** 1
  - `class ContentSkill`
- **Funciones:** 5
  - `def contar_contenido_aleatorio`
  - `def decir_frase_celebre`
  - `def aprender_alias`
  - `def aprender_dato`
  - `def consultar_dato`
- **Variables (Est.):** 14

---

### resources/experiments/whatsapp_to_json.py

- **Líneas:** 73
- **Clases:** 0
- **Funciones:** 1
  - `def parse_whatsapp_chat`
- **Variables (Est.):** 17

---

### modules/utils.py

- **Líneas:** 73
- **Clases:** 0
- **Funciones:** 5
  - `def load_json_data`
  - `def normalize_text`
  - `def number_to_text`
  - `def py_error_handler`
  - `def no_alsa_error`
- **Variables (Est.):** 11

---

### resources/tests/test_cortex.py

- **Líneas:** 72
- **Clases:** 0
- **Funciones:** 0
- **Variables (Est.):** 10

---

### modules/skills/files.py

- **Líneas:** 72
