---
title: استكشاف أخطاء الترقية والترحيل إلى الإدارة المتقدمة للمستودع وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء الترقية والترحيل إلى إدارة المستودعات المتقدمة.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f5bfee31ce27e919086f978fb3ff88ca61a65eba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208077"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="32451-103">استكشاف أخطاء الترقية والترحيل إلى الإدارة المتقدمة للمستودع وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="32451-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32451-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء الترقية والترحيل إلى إدارة المستودعات المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="32451-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="32451-105">أتلقى رسالة الخطا التالية: "java.security.cert.certPathValidatorException: لم يتم العثور علي الثقة التي تم ربطها لمسار الشهادة."</span><span class="sxs-lookup"><span data-stu-id="32451-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="32451-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="32451-106">Issue description</span></span>

<span data-ttu-id="32451-107">تظهر رسالة الخطا هذه في تطبيق المستودع ، وذلك لان الشهادات الموقعة ذاتيا غير موثوق بها في Android 8+ في البيئات المحلية.</span><span class="sxs-lookup"><span data-stu-id="32451-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="32451-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="32451-108">Issue resolution</span></span>

<span data-ttu-id="32451-109">استخدم المرجع المصدق (العام) الخارجي (CA).</span><span class="sxs-lookup"><span data-stu-id="32451-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="32451-110">يتوفر إصلاح لهذه المشكلة في إصدار 1.9.0.0 تطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="32451-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="32451-111">لمزيد من المعلومات حول هذه المشكلة وكيفيه حلها ، راجع [استكشاف مشكلات الاتصال بتطبيق المستودع وإصلاحها](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="32451-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="32451-112">ما هي العملية المعتمدة للتنقل من التخزين الأساسي إلى التخزين المتقدم؟</span><span class="sxs-lookup"><span data-stu-id="32451-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="32451-113">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="32451-113">Issue description</span></span>

<span data-ttu-id="32451-114">أنت تعمل حاليا ضمن أداره المخزون/المخزون وباستخدام وظيفة الأسهم الاساسيه ، وتريد الانتقال إلى التخزين المتقدم للاستفادة من الاجهزه المحمولة والأمواج والعمل.</span><span class="sxs-lookup"><span data-stu-id="32451-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="32451-115">ومع ذلك ، تواجه مشكلات عند محاولة القيام بهذا النقل.</span><span class="sxs-lookup"><span data-stu-id="32451-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="32451-116">علي سبيل المثال ، لا يمكنك تغيير منتجاتك بحيث تستخدم ابعاد التخزين (الموقع والمستودع والموقع) ، نظرا لان المنتجات تحتوي علي حركات مقابله.</span><span class="sxs-lookup"><span data-stu-id="32451-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="32451-117">لذلك، يجب أن تتعلم العملية المعتمدة للتنقل من التخزين الأساسي إلى التخزين المتقدم.</span><span class="sxs-lookup"><span data-stu-id="32451-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="32451-118">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="32451-118">Issue resolution</span></span>

<span data-ttu-id="32451-119">لمزيد من المعلومات حول عمليه النقل من التخزين الأساسي إلى التخزين المتقدم ، راجع النشرات الخاصة بالمدونة والوثائق:</span><span class="sxs-lookup"><span data-stu-id="32451-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="32451-120">تمكين عملية إدارة المستودعات للأصناف والمستودعات الموجودة</span><span class="sxs-lookup"><span data-stu-id="32451-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="32451-121">ترحيل Microsoft Dynamics AX WMS إلى مستودع R3 جديد ووظيفة نقل</span><span class="sxs-lookup"><span data-stu-id="32451-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="32451-122">ترحيل بند WMSI/WMS2</span><span class="sxs-lookup"><span data-stu-id="32451-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="32451-123">ترقية إدارة المستودعات من Microsoft Dynamics AX 2012 to Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="32451-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]