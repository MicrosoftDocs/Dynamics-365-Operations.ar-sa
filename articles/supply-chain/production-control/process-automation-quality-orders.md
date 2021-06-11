---
title: استدعاء تدفقات التشغيل التلقائي للعمليات لإنشاء أوامر الجودة
description: يقدم هذا الموضوع موارد لاستخدام Power Automate لتنفيذ العمليات التجارية تلقائيًا، باستخدام مثال أوامر الجودة.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115159"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="91a82-103">استدعاء تدفقات التشغيل التلقائي للعمليات لإنشاء أوامر الجودة</span><span class="sxs-lookup"><span data-stu-id="91a82-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="91a82-104">ويكون للمؤسسات طلب متزايد لتنفيذ العمليات التجارية القياسية تلقائيًا، وتوفير تعاملات أكثر ملائمة للفريق، واستخدام العديد من إشارات البيانات والأنظمة لمعالجة العمليات التجارية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="91a82-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="91a82-105">باستخدام التشغيل التلقائي للعمليات (RPA) و Microsoft Power Automate، يمكن للأعمال استخدام تجربة بدون كود لتنفيذ العمليات المتكررة تلقائيًا، ومن ثم الحصول على الكفاءة والدقة.</span><span class="sxs-lookup"><span data-stu-id="91a82-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="91a82-106">يعرض قالب حل التشغيل التلقائي القابل للتنزيل لـ Supply Chain Management الكيفية التي يمكن بها استخدام Power Automate لتنفيذ العمليات التجارية تلقائيًا باستخدام أوامر الجودة كمثال.</span><span class="sxs-lookup"><span data-stu-id="91a82-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="91a82-107">يمكنك تنزيل قالب حل التشغيل التلقائي [هنا](https://aka.ms/D365SCMQualityOrderRPASolution).</span><span class="sxs-lookup"><span data-stu-id="91a82-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="91a82-108">للحصول على نظرة عامة حول هذه الميزة والقدرات الخاصة بها، راجع الفيديو التالي: [استخدام RPA لإنشاء أوامر جودة في Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="91a82-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="91a82-109">![خيارات التشغيل التلقائي مع RPA](media/rpa-automation-options.png "خيارات التشغيل التلقائي مع RPA")</span><span class="sxs-lookup"><span data-stu-id="91a82-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="91a82-110">يتضمن قالب حل Power Automate تدفق تنفيذ تلقائي لمجموعة وتدفق التشغيل التلقائي لسطح المكتب والذي يقوم بالتشغيل التلقائي بإنشاء أوامر الجودة في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="91a82-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="91a82-111">يمكن بدء التشغيل التلقائي كاستجابة للعديد من الأحداث والإشارات، بما في ذلك الإشارات الخاصة بإدخال المستخدم أو الجهاز (بما في ذلك إنترنت الأشياء (IoT)).</span><span class="sxs-lookup"><span data-stu-id="91a82-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="91a82-112">يتم تضمين تطبيق Power *Q-Order* في قالب الحل.</span><span class="sxs-lookup"><span data-stu-id="91a82-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="91a82-113">يسمح للمستخدم بمسح كود QR للصنف، وإدخال الكمية وإرفاق الصور باستخدام كاميرا.</span><span class="sxs-lookup"><span data-stu-id="91a82-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="91a82-114">يتم تضمين معلمات الحل لتكوين التشغيل التلقائي لحالة استخدام معينة في تسهيل الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="91a82-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="91a82-115">![إنشاء أمر الجودة](media/rpa-create-quality-roder.png "إنشاء أمر الجودة")</span><span class="sxs-lookup"><span data-stu-id="91a82-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="91a82-116">للحصول على دليل كامل خطوة بخطوة حول كيفية تنزيل حل نموذج وتثبيته واستخدامه للتشغيل التلقائي لإنشاء أمر الجودة، راجع [‬‏‫التشغيل التلقائي لإنشاء أمر الجودة على Dynamics 365 Supply Chain Management بواسطة التشغيل التلقائي للعمليات Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="91a82-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

