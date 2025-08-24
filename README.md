# 🐒 monit-setup

> *"Чтобы всё падало красиво, надо, чтобы кто-то смотрел."*  

Этот репозиторий — маленькая магия для тех, кто не хочет сидеть ночами и следить за своим сервером.  
**Monit** будет смотреть, а ты будешь спать.  

---

## 🚀 Что это?

- Простая (пока что) ansible-role для настройки **Monit**  
- Следим, чтобы Nginx не падал, а если упал — поднимаем за шкирку  
- С минимальным количеством боли и максимальным количеством %^#$@!

---

## 🔧 Как поднять?

* Стягиваем репо:
```bash
git clone https://github.com/yarustina/monit-setup.git
```
* Рисуем any playbook:
```yaml
---
- name: Setup monit playbook
  hosts: all

  roles:
    - role: YOURPATH/TO/ROLES/monit-setup # либо передай путь в ansible.cfg -> roles_path = YOURPATH/TO/ROLES
```
* Запуск:
```bash
ansible-playbook playbook.yml -i YOURPATH/TO/INVENTORY.yml --diff
```

> TL;DR: укажи инвентори, подсунь роль, запусти плейбук — и спи спокойно.

# To-Do

- Доведение шаблона под универсальный формат - возможность генерировать конфиги под оюбые сервисы силами jinja + loop_списка_сервисов 
