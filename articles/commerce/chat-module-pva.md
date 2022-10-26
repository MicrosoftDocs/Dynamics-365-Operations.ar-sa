---
title: التجارة الدردشة مع Power Virtual Agents وحدة
description: توضح هذه المقالة محادثه التجارة مع Power Virtual Agents الوحدة النمطية التي تتكامل مع Microsoft Power Virtual Agents علي المواقع Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691042"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>التجارة الدردشة مع Power Virtual Agents وحدة

[!include [banner](includes/banner.md)]

توضح هذه المقالة محادثه التجارة مع Power Virtual Agents الوحدة النمطية التي تتكامل مع Microsoft Power Virtual Agents علي المواقع Dynamics 365 Commerce.

محادثه التجارة مع Power Virtual Agents ميزه لمنظم Dynamics 365-عملاء التجارة الكترونيه لاستخدام Power Virtual Agents إمكانيات تشاتبوت لمعالجه الاستعلامات الخاصة بهم. واعتبارا من الإصدار ال10.0.30 Dynamics 365 Commerce ، يمكن دمج هذه الميزة في مواقع ويب الخاصة بالتجارة الكترونيه باستخدام المحادثة التجارية مع Power Virtual Agents الوحدة النمطية التي تعد جزءا من مكتبه الوحدة النمطية التجارية.

يساعد محادثه التجارة مع Power Virtual Agents الميزة الاعمال علي تحقيق الأهداف التالية:

- زيادة المشاركة الشخصية مع المستهلكين وتحسين الاحتفاظ بهم.
- زيادة خدمة العملاء من خلال تكامل روبوتات الدردشة ذاتية الخدمة.
- زيادة رضا العملاء بشكل عام ، وبالتالي زيادة المبيعات.

> [!NOTE]
> لمعرفه الاختلافات بين Dynamics 365 أومنيتشانيل لخدمه وتطبيقات Power Virtual Agents العملاء ، راجع [نظره عامه حول ](/commerce-chat-modules-overview.md) الوحدات النمطية للمحادثة التجارية.

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>المتطلبات الأساسية لاستخدام Power Virtual Agents

لاستخدام محادثه التجارة مع Power Virtual Agents ميزه ، يجب أولا إنشاء Power Virtual Agents تشاتبوت لموقع ويب الخاص بالتجارة الكترونيه. للحصول علي الإرشادات ، راجع [إنشاء بوت](/power-virtual-agents/authoring-first-bot) "عامل الطاقة الظاهرية".

بعد تكوين تشاتبوت ، يجب نسخ قيم **معرف** بوت ومعلمه تشاتبوت معرف **المستاجرين** لتكوين تجربه المحادثة التجارية. للحصول علي معلومات حول كيفيه نسخ هذه القيم ، راجع [استرداد معلمات Power Virtual Agents بوت الخاصة بك](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>تكوين موقع التجارة الإلكترونية الخاص بك 

إحدى الطرق الموصى بها لتنفيذ تجربة الدردشة لموقع التجارة الإلكترونية الخاص بك هي إضافة Commerce Chat with Power Virtual Agents الوحدة النمطية لجزء الرأس المشترك المستخدم في صفحات موقعك.

لإضافة وحدة الدردشة إلى جزء رأس موقعك في Commerce Site Builder ، اتبع هذه الخطوات.

1. في منشئ موقع التجارة لموقعك ، انتقل إلى **Fragments**.
1. حدد **جديد**.
1. في **حدد جزء** في مربع الحوار ، حدد ملف **التجارة الدردشة مع Power Virtual Agents** الوحدة النمطية ، أدخل اسمًا للجزء ، ثم حدد **موافق**.
1. في عرض المخطط التفصيلي ، حدد **فتحه موصل** Msdyn365 pva chat
1. في جزء الخصائص على اليسار ، اتبع الخطوات التالية:

    1. ضمن **معلمات** بوت ، في الحقل ويبتشات الخاص **Bot Framework بCDN** محادثت ، اترك القيمة الافتراضية (علي سبيل المثال ، `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. في **Bot Framework Direct Line عنوان URL للمصادقة** ، اترك القيمة الافتراضية (على سبيل المثال ، `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. في **معرف البوت** الحقل ، أدخل Power Virtual Agents **معرف البوت** القيمة التي نسختها في ملف [المتطلبات الأساسية لاستخدام Power Virtual Agents](#prereq) جزء.
    1. في الحقل معرف **المستاجر** ، ادخل **قيمه معرف** المستاجر التي قمت بنسخها.

1. حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.
1. انتقل إلى **أجزاء** ، وافتح جزء الراس الخاص بموقعك.
1. في فتحة **الحاوية الافتراضية‬‬‏‫** ، حدد علامة القطع (**...**)، ثم حدد **إضافة جزء**.
1. في مربع الحوار **تحديد الوحدات** ، حدد جزء المحادثة الذي قمت بإنشائه مسبقًا ، ثم حدد **موافق**.
1. حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الجزء، ثم حدد **نشر** لنشره.

## <a name="proactive-chat-parameters"></a>معلمات الدردشة الاستباقية

للحصول على قائمة كاملة بمعلمات تكوين الدردشة الاستباقية ، راجع [وحده المحادثة التجارية النمطية معلمات](chat-proactive-chat-parameters.md)المحادثة الاستباقية.

> [!NOTE]
> حالياً, Power Virtual Agents لا يدعم Azure Active Directory B2C (Azure AD B2C) المصادقة. يدعم فقط استدعاءات (ركسو) المجهولة Retail Cloud Scale Unit للحصول علي توفر المنتجات أو التفاعل مع واجات api المجهولة الأخرى. تتطلب الاستدعاءات إلى واجات برمجه التطبيقات (Api) المصادق من خلال Power Virtual Agents تشاتبوتس تسجيل دخول عميل صريح.

## <a name="additional-resources"></a>الموارد الإضافية

[نظره عامه حول ميزات المحادثة التجارية](commerce-chat-overview.md)

[محادثه تجاره مع أومنيتشانيل للوحدة النمطية لخدمه العملاء](commerce-chat-module.md)

[وحده دردشة التجارة ، محددات المحادثة الاستباقية](chat-proactive-chat-parameters.md)
