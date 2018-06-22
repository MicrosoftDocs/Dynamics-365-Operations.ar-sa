---
title: "توزيع المستندات الواردة في Microsoft Excel"
description: "يوفر هذا الموضوع معلومات حول تنسيقات تصميم إعداد التقارير الإلكترونية (ER) لتوزيع المعلومات الواردة في ملفات Microsoft Excel الواردة."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 001e287590b9f43ed38de803bcace3a25a6f6637
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2018

---

# <a name="parse-incoming-microsoft-excel-files"></a><span data-ttu-id="5c63b-103">توزيع مستندات Microsoft Excel الواردة</span><span class="sxs-lookup"><span data-stu-id="5c63b-103">Parse incoming Microsoft Excel files</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5c63b-104">يمكنك تصميم الإلكتروني تقارير تنسيقات إعداد التقارير الإلكترونية (ER) Excel لتوزيع ملفات Microsoft Excel الواردة التي تمثل البيانات في مصنفات Microsoft Excel (الملفات بتنسيق XLSX).</span><span class="sxs-lookup"><span data-stu-id="5c63b-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="5c63b-105">يمكنك بعد ذلك استخدام المحتوى من هذه الملفات لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="5c63b-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="5c63b-106">ويكون هذا مفيدًا في حالة:</span><span class="sxs-lookup"><span data-stu-id="5c63b-106">This is useful if you:</span></span>

-   <span data-ttu-id="5c63b-107">تصميم نموذج جديد وتنسيق، واختبارهم في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="5c63b-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="5c63b-108">في هذه الحالة، سوف يقوم Excel بمحاكاة بيانات التطبيق الفعلية.</span><span class="sxs-lookup"><span data-stu-id="5c63b-108">In this case, Excel will simulate the actual application data.</span></span>
-   <span data-ttu-id="5c63b-109">إدارة بيانات تتجاوز تطبيقك في Excel وتريد استيراد هذه البيانات لإرسال تقرير مُحدد.</span><span class="sxs-lookup"><span data-stu-id="5c63b-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="5c63b-110">لمزيد من المعلومات حول هذه الميزة، قم بتشغيل دليل المهام **استيراد بيانات ER من ملف Microsoft Excel (الجزء الأول: تصميم التنسيق)** و **استيراد بيانات ER من ملف Microsoft Excel (الجزء 2: استيراد البيانات)** (الأجزاء من 7.5.4.3 الحصول على/تطوير مكونات خدمة/حل تكنولوجيا المعلومات (10677) العملية التجارية).</span><span class="sxs-lookup"><span data-stu-id="5c63b-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="5c63b-111">تتناول دلائل المهام هذه كيف يمكن نشر ملف Excel وارد باستخدام تنسيق ER لاستيراد معلومات من المستندات الواردة وتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="5c63b-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="5c63b-112">يمكنك تحميل ملفات دليل المهام من [مركز تحميل Microsoft](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="5c63b-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="5c63b-113">قم بتنزيل الملفات التالية لإكمال دلائل المهام المذكورة أعلاه.</span><span class="sxs-lookup"><span data-stu-id="5c63b-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="5c63b-114">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="5c63b-114">Content description</span></span>                        | <span data-ttu-id="5c63b-115">ملف</span><span class="sxs-lookup"><span data-stu-id="5c63b-115">File</span></span>                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="5c63b-116">ملف وارد بتنسيق XLSX- قالب</span><span class="sxs-lookup"><span data-stu-id="5c63b-116">Incoming file in .XLSX format - template</span></span>   | [<span data-ttu-id="5c63b-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="5c63b-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)  |
| <span data-ttu-id="5c63b-118">ملف وارد بتنسيق XLSX- بيانات نموذجية</span><span class="sxs-lookup"><span data-stu-id="5c63b-118">Incoming file in .XLSX format - sample data</span></span>| [<span data-ttu-id="5c63b-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="5c63b-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="5c63b-120">إذا لم تقم بتشغيل دليل المهام التالي بعد، [‏‫التقارير الإلكترونية - إنشاء التكوينات المطلوبة لاستيراد البيانات من ملف خارجي‬](./tasks/er-required-configurations-import-data.md) في تطبيق Dynamics 365 for Finance and Operation الحالي، قم بتنزيل الملف التالي.</span><span class="sxs-lookup"><span data-stu-id="5c63b-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="5c63b-121">وصف المحتوى</span><span class="sxs-lookup"><span data-stu-id="5c63b-121">Content description</span></span>                        | <span data-ttu-id="5c63b-122">ملف</span><span class="sxs-lookup"><span data-stu-id="5c63b-122">File</span></span>                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="5c63b-123">تكوين نموذج تقارير إلكترونية</span><span class="sxs-lookup"><span data-stu-id="5c63b-123">ER model configuration</span></span>                     | [<span data-ttu-id="5c63b-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="5c63b-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)            |


