---
title: التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وDataverse
description: يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: af746d1d20ddd1552bce797288c6d62d69d7bd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748839"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="f807a-103">التحقق من تكوين الكتابة المزدوجة في تطبيقات Finance and Operations وDataverse</span><span class="sxs-lookup"><span data-stu-id="f807a-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="f807a-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="f807a-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="f807a-105">على وجه التحديد، يشرح هذا الموضوع كيفية تحديد ما إذا كان قد تم تكوين الكتابة الثنائية في تطبيقات Finance and Operations وفي Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f807a-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="f807a-106">التحقق من تكوين الكتابة الثنائية في تطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f807a-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="f807a-107">لتحديد ما إذا كانت الأخطاء التي تراها عند محاولة حفظ الصفوف للتحديث تاتي من الكتابة الثنائية أو لا، تحقق أولاً من تكوين الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="f807a-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="f807a-108">إذا كانت لديك امتيازات إدارية في تطبيق Finance and Operations، فانتقل إلى **مساحات العمل\> إدارة البيانات**، وحدد تجانب **الكتابة الثنائية**.</span><span class="sxs-lookup"><span data-stu-id="f807a-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="f807a-109">في حالة عرض تفاصيل البيئات المرتبطة وقائمة مخططات الجداول قيد التشغيل، فإنه يتم تكوين الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="f807a-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![التحقق من اتصال تطبيق Finance and Operationsعندما يكون لديك امتيازات المسؤول](media/verify_fin_ops_1.png)

+ <span data-ttu-id="f807a-111">إذا لم يكن لديك امتيازات المسؤول، فستتلقى رسالة خطأ، *لا يمكن كتابة البيانات إلى كيان \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="f807a-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="f807a-112">في المثال الموجود في التوضيح التالي، لا يمكنك إنشاء صف عميل في تطبيق Finance and Operations، لأنه يتم تكوين الكتابة الثنائية، ولكن لا توجد البيانات المرجعية لشروط الدفع ومجموعة العملاء في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f807a-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![التحقق من اتصال تطبيق Finance and Operationsعندما لا يكون لديك امتيازات المسؤول](media/verify_fin_ops_2.png)

<span data-ttu-id="f807a-114">للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في تطبيقات Finance and Operations، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="f807a-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="f807a-115">التحقق من تكوين الكتابة الثنائية في Dataverse</span><span class="sxs-lookup"><span data-stu-id="f807a-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="f807a-116">عندما تقوم بإنشاء بيانات، إذا شاهدت عمود **الشركة** في صفحات في Dataverse، فإنه يتم تكوين الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="f807a-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![التحقق من اتصال Dataverse](media/verify_cds.png)

<span data-ttu-id="f807a-118">للحصول على معلومات حول كيفية إصلاح المشكلات عند قيامك بإنشاء البيانات في Dataverse، راجع [استكشاف مشكلات المزامنة المباشرة وإصلاحها](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="f807a-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="f807a-119">للحصول على معلومات حول كيفية عرض تفاصيل الأخطاء في حالة مصادفة أي أخطاء اثناء إنشاء البيانات في Dataverse، راجع [تمكين وعرض تسجيل تتبع المكونات الإضافية في Dataverse لعرض تفاصيل الأخطاء](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="f807a-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]